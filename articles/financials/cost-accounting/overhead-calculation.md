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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841497"
---
# <a name="overhead-calculation"></a><span data-ttu-id="1e1cb-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="1e1cb-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e1cb-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="1e1cb-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-105">Term definition</span></span>
---------------

<span data-ttu-id="1e1cb-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="1e1cb-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="1e1cb-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="1e1cb-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="1e1cb-109">Rent</span></span>
-   <span data-ttu-id="1e1cb-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-110">Electricity</span></span>
-   <span data-ttu-id="1e1cb-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="1e1cb-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="1e1cb-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="1e1cb-112">Overhead calculation overview</span></span>
<span data-ttu-id="1e1cb-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="1e1cb-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="1e1cb-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="1e1cb-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="1e1cb-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="1e1cb-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="1e1cb-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="1e1cb-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="1e1cb-119">Version type</span></span>
-   <span data-ttu-id="1e1cb-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="1e1cb-120">Date and time</span></span>
-   <span data-ttu-id="1e1cb-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="1e1cb-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="1e1cb-122">Fiscal year</span></span>
-   <span data-ttu-id="1e1cb-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="1e1cb-123">Fiscal period</span></span>

<span data-ttu-id="1e1cb-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="1e1cb-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="1e1cb-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="1e1cb-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="1e1cb-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="1e1cb-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="1e1cb-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="1e1cb-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="1e1cb-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="1e1cb-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="1e1cb-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="1e1cb-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="1e1cb-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="1e1cb-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="1e1cb-140">Main account</span></span></th>
<th><span data-ttu-id="1e1cb-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="1e1cb-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-143">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-143">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-144">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-145">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-145">10001</span></span></td>
<td><span data-ttu-id="1e1cb-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-146">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="1e1cb-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="1e1cb-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="1e1cb-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="1e1cb-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-151">Define the cost behavior rule</span></span>

<span data-ttu-id="1e1cb-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="1e1cb-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="1e1cb-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="1e1cb-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="1e1cb-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="1e1cb-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="1e1cb-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="1e1cb-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="1e1cb-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-160">Journal</span></span></th>
<th><span data-ttu-id="1e1cb-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="1e1cb-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e1cb-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="1e1cb-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e1cb-163">Версия</span><span class="sxs-lookup"><span data-stu-id="1e1cb-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-164">00001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-164">00001</span></span></td>
<td><span data-ttu-id="1e1cb-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="1e1cb-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="1e1cb-166">Fiscal</span></span></td>
<td><span data-ttu-id="1e1cb-167">2017</span><span class="sxs-lookup"><span data-stu-id="1e1cb-167">2017</span></span></td>
<td><span data-ttu-id="1e1cb-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-168">Period 1</span></span></td>
<td><span data-ttu-id="1e1cb-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e1cb-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-173">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-174">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-177">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-177">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-178">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-179">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-179">10001</span></span></td>
<td><span data-ttu-id="1e1cb-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-180">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="1e1cb-181">Unclassified</span></span></td>
<td><span data-ttu-id="1e1cb-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e1cb-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-185">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-186">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-187">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-189">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-189">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-190">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-191">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-191">10001</span></span></td>
<td><span data-ttu-id="1e1cb-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-192">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="1e1cb-193">Unclassified</span></span></td>
<td><span data-ttu-id="1e1cb-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-194">10,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-196">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-196">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-197">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-198">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-198">10001</span></span></td>
<td><span data-ttu-id="1e1cb-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-199">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="1e1cb-200">Unclassified</span></span></td>
<td><span data-ttu-id="1e1cb-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-201">-10,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-203">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-203">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-204">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-205">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-205">10001</span></span></td>
<td><span data-ttu-id="1e1cb-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-206">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-207">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-208">1,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-210">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-210">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-211">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-212">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-212">10001</span></span></td>
<td><span data-ttu-id="1e1cb-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-213">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-214">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-215">9,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="1e1cb-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="1e1cb-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="1e1cb-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="1e1cb-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-221">Define the cost distribution rule</span></span>

<span data-ttu-id="1e1cb-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="1e1cb-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="1e1cb-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="1e1cb-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="1e1cb-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="1e1cb-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-228">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="1e1cb-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-230">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-230">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-231">HR</span></span></td>
<td><span data-ttu-id="1e1cb-232">1000</span><span class="sxs-lookup"><span data-stu-id="1e1cb-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-233">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-233">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-234">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-235">6,000</span><span class="sxs-lookup"><span data-stu-id="1e1cb-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-236">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-236">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-237">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-238">0</span><span class="sxs-lookup"><span data-stu-id="1e1cb-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-240">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-241">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-241">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-242">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-244">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-244">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-245">HR</span></span></td>
<td><span data-ttu-id="1e1cb-246">1000</span><span class="sxs-lookup"><span data-stu-id="1e1cb-246">1,000</span></span></td>
<td><span data-ttu-id="1e1cb-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-249">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-249">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-250">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-251">6,000</span><span class="sxs-lookup"><span data-stu-id="1e1cb-251">6,000</span></span></td>
<td><span data-ttu-id="1e1cb-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1e1cb-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-254">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-254">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-255">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-256">0</span><span class="sxs-lookup"><span data-stu-id="1e1cb-256">0</span></span></td>
<td><span data-ttu-id="1e1cb-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-258">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="1e1cb-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-261">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-262">Формула</span><span class="sxs-lookup"><span data-stu-id="1e1cb-262">Formula</span></span></th>
<th><span data-ttu-id="1e1cb-263">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-263">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-264">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-266">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-266">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-267">HR</span></span></td>
<td><span data-ttu-id="1e1cb-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e1cb-269">1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-269">1</span></span></td>
<td><span data-ttu-id="1e1cb-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-271">500.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-272">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-272">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-273">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e1cb-275">1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-275">1</span></span></td>
<td><span data-ttu-id="1e1cb-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-277">500.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-278">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-278">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-279">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1e1cb-281">0</span><span class="sxs-lookup"><span data-stu-id="1e1cb-281">0</span></span></td>
<td><span data-ttu-id="1e1cb-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-283">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1e1cb-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-285">Journal</span></span></th>
<th><span data-ttu-id="1e1cb-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="1e1cb-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e1cb-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="1e1cb-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e1cb-288">Версия</span><span class="sxs-lookup"><span data-stu-id="1e1cb-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-289">00002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-289">00002</span></span></td>
<td><span data-ttu-id="1e1cb-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="1e1cb-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="1e1cb-291">Fiscal</span></span></td>
<td><span data-ttu-id="1e1cb-292">2017</span><span class="sxs-lookup"><span data-stu-id="1e1cb-292">2017</span></span></td>
<td><span data-ttu-id="1e1cb-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-293">Period 1</span></span></td>
<td><span data-ttu-id="1e1cb-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e1cb-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-298">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-299">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-302">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-302">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-303">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-304">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-304">10001</span></span></td>
<td><span data-ttu-id="1e1cb-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-305">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-306">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-309">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-309">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-310">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-311">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-311">10001</span></span></td>
<td><span data-ttu-id="1e1cb-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-312">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-313">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e1cb-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-317">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-318">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-319">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-321">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-321">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-322">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-323">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-323">10001</span></span></td>
<td><span data-ttu-id="1e1cb-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-324">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-325">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-326">-1,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-328">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-328">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-329">HR</span></span></td>
<td><span data-ttu-id="1e1cb-330">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-330">10001</span></span></td>
<td><span data-ttu-id="1e1cb-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-331">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-332">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-333">500.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-333">500.00</span></span></td>
<td><span data-ttu-id="1e1cb-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-335">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-335">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-336">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-337">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-337">10001</span></span></td>
<td><span data-ttu-id="1e1cb-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-338">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-339">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-340">500.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-340">500.00</span></span></td>
<td><span data-ttu-id="1e1cb-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-342">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-342">CC099</span></span></td>
<td><span data-ttu-id="1e1cb-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e1cb-343">Default cost center</span></span></td>
<td><span data-ttu-id="1e1cb-344">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-344">10001</span></span></td>
<td><span data-ttu-id="1e1cb-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-345">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-346">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-347">-9,000.00</span></span></td>
<td><span data-ttu-id="1e1cb-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-349">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-349">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-350">HR</span></span></td>
<td><span data-ttu-id="1e1cb-351">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-351">10001</span></span></td>
<td><span data-ttu-id="1e1cb-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-352">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-353">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-354">1,285.71</span></span></td>
<td><span data-ttu-id="1e1cb-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-356">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-356">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-357">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-358">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-358">10001</span></span></td>
<td><span data-ttu-id="1e1cb-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-359">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-360">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1e1cb-361">7,714.29</span></span></td>
<td><span data-ttu-id="1e1cb-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="1e1cb-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="1e1cb-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="1e1cb-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="1e1cb-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="1e1cb-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="1e1cb-367">Define the overhead rate</span></span>

<span data-ttu-id="1e1cb-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="1e1cb-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-370">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-371">Часы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-372">Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-373">Project 1</span></span></td>
<td><span data-ttu-id="1e1cb-374">3</span><span class="sxs-lookup"><span data-stu-id="1e1cb-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-375">Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-376">Project 2</span></span></td>
<td><span data-ttu-id="1e1cb-377">1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-379">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-380">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-381">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-382">Units</span></span></th>
<th><span data-ttu-id="1e1cb-383">По норме</span><span class="sxs-lookup"><span data-stu-id="1e1cb-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-384">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-384">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-385">HR</span></span></td>
<td><span data-ttu-id="1e1cb-386">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-386">10001</span></span></td>
<td><span data-ttu-id="1e1cb-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-387">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-388">1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-388">1</span></span></td>
<td><span data-ttu-id="1e1cb-389">10</span><span class="sxs-lookup"><span data-stu-id="1e1cb-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-391">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-392">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-392">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-393">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-394">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-396">Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-397">Project 1</span></span></td>
<td><span data-ttu-id="1e1cb-398">3</span><span class="sxs-lookup"><span data-stu-id="1e1cb-398">3</span></span></td>
<td><span data-ttu-id="1e1cb-399">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-399">10001</span></span></td>
<td><span data-ttu-id="1e1cb-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1e1cb-401">30.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-402">Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-403">Project 2</span></span></td>
<td><span data-ttu-id="1e1cb-404">1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-404">1</span></span></td>
<td><span data-ttu-id="1e1cb-405">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-405">10001</span></span></td>
<td><span data-ttu-id="1e1cb-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1e1cb-407">10,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1e1cb-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-409">Journal</span></span></th>
<th><span data-ttu-id="1e1cb-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="1e1cb-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e1cb-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="1e1cb-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e1cb-412">Версия</span><span class="sxs-lookup"><span data-stu-id="1e1cb-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-413">00003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-413">00003</span></span></td>
<td><span data-ttu-id="1e1cb-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="1e1cb-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="1e1cb-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="1e1cb-415">Fiscal</span></span></td>
<td><span data-ttu-id="1e1cb-416">2017</span><span class="sxs-lookup"><span data-stu-id="1e1cb-416">2017</span></span></td>
<td><span data-ttu-id="1e1cb-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-417">Period 1</span></span></td>
<td><span data-ttu-id="1e1cb-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="1e1cb-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-421">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-422">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-424">Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-426">3,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-428">Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-430">1.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e1cb-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-433">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-434">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-435">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-437">CC0001</span></span></td>
<td><span data-ttu-id="1e1cb-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-438">HR</span></span></td>
<td><span data-ttu-id="1e1cb-439">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-439">10001</span></span></td>
<td><span data-ttu-id="1e1cb-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-440">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-441">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-442">-30.00</span></span></td>
<td><span data-ttu-id="1e1cb-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-444">Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1e1cb-446">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-446">10001</span></span></td>
<td><span data-ttu-id="1e1cb-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-447">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-448">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-449">30.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-449">30.00</span></span></td>
<td><span data-ttu-id="1e1cb-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-451">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-451">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-452">HR</span></span></td>
<td><span data-ttu-id="1e1cb-453">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-453">10001</span></span></td>
<td><span data-ttu-id="1e1cb-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-454">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-455">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-456">-10.00</span></span></td>
<td><span data-ttu-id="1e1cb-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-458">Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1e1cb-460">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-460">10001</span></span></td>
<td><span data-ttu-id="1e1cb-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-461">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-462">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-463">10.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-463">10.00</span></span></td>
<td><span data-ttu-id="1e1cb-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="1e1cb-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="1e1cb-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="1e1cb-468">Finance and Operations поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="1e1cb-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="1e1cb-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="1e1cb-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="1e1cb-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="1e1cb-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="1e1cb-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="1e1cb-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-475">Define the cost allocation</span></span>

<span data-ttu-id="1e1cb-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="1e1cb-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="1e1cb-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-479">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-481">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-481">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-482">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-483">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-484">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-484">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-485">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-486">55</span><span class="sxs-lookup"><span data-stu-id="1e1cb-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-487">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-487">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-488">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-489">10</span><span class="sxs-lookup"><span data-stu-id="1e1cb-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="1e1cb-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-492">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="1e1cb-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-494">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-494">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-495">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-496">65</span><span class="sxs-lookup"><span data-stu-id="1e1cb-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-497">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-497">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-498">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-499">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="1e1cb-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-502">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-504">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-505">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-506">60</span><span class="sxs-lookup"><span data-stu-id="1e1cb-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-507">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-508">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-509">20</span><span class="sxs-lookup"><span data-stu-id="1e1cb-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="1e1cb-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-512">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-514">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-515">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-516">80</span><span class="sxs-lookup"><span data-stu-id="1e1cb-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-517">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-518">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-519">15</span><span class="sxs-lookup"><span data-stu-id="1e1cb-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e1cb-520">В Finance and Operations статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="1e1cb-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="1e1cb-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-523">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-524">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-524">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-525">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-526">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-528">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-528">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-529">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-530">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-530">35</span></span></td>
<td><span data-ttu-id="1e1cb-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e1cb-532">175.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-532">175.00</span></span></td>
<td><span data-ttu-id="1e1cb-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-534">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-534">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-535">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-536">55</span><span class="sxs-lookup"><span data-stu-id="1e1cb-536">55</span></span></td>
<td><span data-ttu-id="1e1cb-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e1cb-538">275.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-538">275.00</span></span></td>
<td><span data-ttu-id="1e1cb-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-540">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-540">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-541">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-542">10</span><span class="sxs-lookup"><span data-stu-id="1e1cb-542">10</span></span></td>
<td><span data-ttu-id="1e1cb-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1e1cb-544">50,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-544">50.00</span></span></td>
<td><span data-ttu-id="1e1cb-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-546">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-546">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-547">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-548">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-548">35</span></span></td>
<td><span data-ttu-id="1e1cb-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e1cb-550">436.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-550">436.00</span></span></td>
<td><span data-ttu-id="1e1cb-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-552">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-552">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-553">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-554">55</span><span class="sxs-lookup"><span data-stu-id="1e1cb-554">55</span></span></td>
<td><span data-ttu-id="1e1cb-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e1cb-556">685.14</span><span class="sxs-lookup"><span data-stu-id="1e1cb-556">685.14</span></span></td>
<td><span data-ttu-id="1e1cb-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-558">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-558">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-559">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-560">10</span><span class="sxs-lookup"><span data-stu-id="1e1cb-560">10</span></span></td>
<td><span data-ttu-id="1e1cb-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1e1cb-562">124.57</span><span class="sxs-lookup"><span data-stu-id="1e1cb-562">124.57</span></span></td>
<td><span data-ttu-id="1e1cb-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-565">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-566">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-566">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-567">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-568">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-570">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-570">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-571">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-572">65</span><span class="sxs-lookup"><span data-stu-id="1e1cb-572">65</span></span></td>
<td><span data-ttu-id="1e1cb-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1e1cb-574">438.75</span><span class="sxs-lookup"><span data-stu-id="1e1cb-574">438.75</span></span></td>
<td><span data-ttu-id="1e1cb-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-576">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-576">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-577">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-578">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-578">35</span></span></td>
<td><span data-ttu-id="1e1cb-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1e1cb-580">236.25</span><span class="sxs-lookup"><span data-stu-id="1e1cb-580">236.25</span></span></td>
<td><span data-ttu-id="1e1cb-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-582">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-582">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-583">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-584">65</span><span class="sxs-lookup"><span data-stu-id="1e1cb-584">65</span></span></td>
<td><span data-ttu-id="1e1cb-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1e1cb-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1e1cb-586">5,297.69</span></span></td>
<td><span data-ttu-id="1e1cb-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-588">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-588">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-589">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-590">35</span><span class="sxs-lookup"><span data-stu-id="1e1cb-590">35</span></span></td>
<td><span data-ttu-id="1e1cb-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1e1cb-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1e1cb-592">2,852.60</span></span></td>
<td><span data-ttu-id="1e1cb-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-595">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-596">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-596">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-597">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-598">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-600">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-601">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-602">60</span><span class="sxs-lookup"><span data-stu-id="1e1cb-602">60</span></span></td>
<td><span data-ttu-id="1e1cb-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1e1cb-604">535.31</span><span class="sxs-lookup"><span data-stu-id="1e1cb-604">535.31</span></span></td>
<td><span data-ttu-id="1e1cb-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-606">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-607">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-608">20</span><span class="sxs-lookup"><span data-stu-id="1e1cb-608">20</span></span></td>
<td><span data-ttu-id="1e1cb-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1e1cb-610">178.44</span><span class="sxs-lookup"><span data-stu-id="1e1cb-610">178.44</span></span></td>
<td><span data-ttu-id="1e1cb-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-612">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-613">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-614">60</span><span class="sxs-lookup"><span data-stu-id="1e1cb-614">60</span></span></td>
<td><span data-ttu-id="1e1cb-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1e1cb-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1e1cb-616">4,487.12</span></span></td>
<td><span data-ttu-id="1e1cb-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-618">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-619">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-620">20</span><span class="sxs-lookup"><span data-stu-id="1e1cb-620">20</span></span></td>
<td><span data-ttu-id="1e1cb-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1e1cb-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-622">1,495.71</span></span></td>
<td><span data-ttu-id="1e1cb-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1e1cb-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-625">Cost object</span></span></th>
<th><span data-ttu-id="1e1cb-626">Величина</span><span class="sxs-lookup"><span data-stu-id="1e1cb-626">Magnitude</span></span></th>
<th><span data-ttu-id="1e1cb-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="1e1cb-627">Allocation factor</span></span></th>
<th><span data-ttu-id="1e1cb-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-628">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-630">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-631">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-632">80</span><span class="sxs-lookup"><span data-stu-id="1e1cb-632">80</span></span></td>
<td><span data-ttu-id="1e1cb-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1e1cb-634">241.05</span><span class="sxs-lookup"><span data-stu-id="1e1cb-634">241.05</span></span></td>
<td><span data-ttu-id="1e1cb-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-636">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-637">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-638">15</span><span class="sxs-lookup"><span data-stu-id="1e1cb-638">15</span></span></td>
<td><span data-ttu-id="1e1cb-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1e1cb-640">45.20</span><span class="sxs-lookup"><span data-stu-id="1e1cb-640">45.20</span></span></td>
<td><span data-ttu-id="1e1cb-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-642">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-643">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-644">80</span><span class="sxs-lookup"><span data-stu-id="1e1cb-644">80</span></span></td>
<td><span data-ttu-id="1e1cb-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1e1cb-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1e1cb-646">2,507.09</span></span></td>
<td><span data-ttu-id="1e1cb-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-648">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-649">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-650">15</span><span class="sxs-lookup"><span data-stu-id="1e1cb-650">15</span></span></td>
<td><span data-ttu-id="1e1cb-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1e1cb-652">470.08</span><span class="sxs-lookup"><span data-stu-id="1e1cb-652">470.08</span></span></td>
<td><span data-ttu-id="1e1cb-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1e1cb-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="1e1cb-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="1e1cb-655">Journal</span></span></th>
<th><span data-ttu-id="1e1cb-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="1e1cb-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1e1cb-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="1e1cb-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1e1cb-658">Версия</span><span class="sxs-lookup"><span data-stu-id="1e1cb-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-659">00004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-659">00004</span></span></td>
<td><span data-ttu-id="1e1cb-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="1e1cb-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="1e1cb-661">Fiscal</span></span></td>
<td><span data-ttu-id="1e1cb-662">2017</span><span class="sxs-lookup"><span data-stu-id="1e1cb-662">2017</span></span></td>
<td><span data-ttu-id="1e1cb-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-663">Period 1</span></span></td>
<td><span data-ttu-id="1e1cb-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="1e1cb-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="1e1cb-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1e1cb-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-668">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-669">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-672">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-672">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-673">HR</span></span></td>
<td><span data-ttu-id="1e1cb-674">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-674">10001</span></span></td>
<td><span data-ttu-id="1e1cb-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-675">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-676">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-677">500.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-679">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-679">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-680">HR</span></span></td>
<td><span data-ttu-id="1e1cb-681">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-681">10001</span></span></td>
<td><span data-ttu-id="1e1cb-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-682">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-683">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-686">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-686">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-687">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-688">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-688">10001</span></span></td>
<td><span data-ttu-id="1e1cb-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-689">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-690">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-691">675.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-693">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-693">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-694">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-695">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-695">10001</span></span></td>
<td><span data-ttu-id="1e1cb-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-696">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-697">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="1e1cb-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-700">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-700">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-701">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-702">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-702">10001</span></span></td>
<td><span data-ttu-id="1e1cb-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-703">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-704">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-705">713.75</span><span class="sxs-lookup"><span data-stu-id="1e1cb-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-707">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-707">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-708">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-709">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-709">10001</span></span></td>
<td><span data-ttu-id="1e1cb-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-710">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-711">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="1e1cb-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-714">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-714">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-715">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-716">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-716">10001</span></span></td>
<td><span data-ttu-id="1e1cb-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-717">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-718">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-719">286.25</span><span class="sxs-lookup"><span data-stu-id="1e1cb-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-721">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-721">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-722">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-723">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-723">10001</span></span></td>
<td><span data-ttu-id="1e1cb-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-724">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-725">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="1e1cb-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-728">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-729">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-730">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-730">10001</span></span></td>
<td><span data-ttu-id="1e1cb-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-731">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-732">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-733">776.36</span><span class="sxs-lookup"><span data-stu-id="1e1cb-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-735">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-736">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-737">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-737">10001</span></span></td>
<td><span data-ttu-id="1e1cb-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-738">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-739">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1e1cb-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-742">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-743">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-744">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-744">10001</span></span></td>
<td><span data-ttu-id="1e1cb-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-745">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-746">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-747">223.64</span><span class="sxs-lookup"><span data-stu-id="1e1cb-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="1e1cb-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-749">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-750">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-751">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-751">10001</span></span></td>
<td><span data-ttu-id="1e1cb-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-752">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-753">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1e1cb-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1e1cb-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1e1cb-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1e1cb-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-757">Cost element</span></span></th>
<th><span data-ttu-id="1e1cb-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-758">Cost behavior</span></span></th>
<th><span data-ttu-id="1e1cb-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-759">Amount</span></span></th>
<th><span data-ttu-id="1e1cb-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="1e1cb-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1e1cb-761">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-761">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-762">HR</span></span></td>
<td><span data-ttu-id="1e1cb-763">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-763">10001</span></span></td>
<td><span data-ttu-id="1e1cb-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-764">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-765">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-766">-500.00</span></span></td>
<td><span data-ttu-id="1e1cb-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-768">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-768">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-769">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-770">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-770">10001</span></span></td>
<td><span data-ttu-id="1e1cb-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-771">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-772">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-773">175.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-773">175.00</span></span></td>
<td><span data-ttu-id="1e1cb-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-775">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-775">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-776">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-777">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-777">10001</span></span></td>
<td><span data-ttu-id="1e1cb-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-778">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-779">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-780">275.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-780">275.00</span></span></td>
<td><span data-ttu-id="1e1cb-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-782">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-782">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-783">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-784">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-784">10001</span></span></td>
<td><span data-ttu-id="1e1cb-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-785">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-786">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-787">50,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-787">50,00</span></span></td>
<td><span data-ttu-id="1e1cb-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-789">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-789">CC001</span></span></td>
<td><span data-ttu-id="1e1cb-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="1e1cb-790">HR</span></span></td>
<td><span data-ttu-id="1e1cb-791">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-791">10001</span></span></td>
<td><span data-ttu-id="1e1cb-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-792">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-793">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-794">-1,245.71</span></span></td>
<td><span data-ttu-id="1e1cb-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-796">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-796">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-797">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-798">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-798">10001</span></span></td>
<td><span data-ttu-id="1e1cb-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-799">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-800">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-801">436.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-801">436.00</span></span></td>
<td><span data-ttu-id="1e1cb-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-803">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-803">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-804">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-805">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-805">10001</span></span></td>
<td><span data-ttu-id="1e1cb-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-806">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-807">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-808">685.14</span><span class="sxs-lookup"><span data-stu-id="1e1cb-808">685.14</span></span></td>
<td><span data-ttu-id="1e1cb-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-810">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-810">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-811">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-812">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-812">10001</span></span></td>
<td><span data-ttu-id="1e1cb-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-813">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-814">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-815">124.57</span><span class="sxs-lookup"><span data-stu-id="1e1cb-815">124.57</span></span></td>
<td><span data-ttu-id="1e1cb-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-817">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-817">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-818">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-819">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-819">10001</span></span></td>
<td><span data-ttu-id="1e1cb-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-820">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-821">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-822">-675.00</span></span></td>
<td><span data-ttu-id="1e1cb-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-824">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-824">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-825">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-826">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-826">10001</span></span></td>
<td><span data-ttu-id="1e1cb-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-827">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-828">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-829">438.75</span><span class="sxs-lookup"><span data-stu-id="1e1cb-829">438.75</span></span></td>
<td><span data-ttu-id="1e1cb-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-831">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-831">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-832">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-833">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-833">10001</span></span></td>
<td><span data-ttu-id="1e1cb-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-834">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-835">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-836">236.25</span><span class="sxs-lookup"><span data-stu-id="1e1cb-836">236.25</span></span></td>
<td><span data-ttu-id="1e1cb-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-838">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-838">CC002</span></span></td>
<td><span data-ttu-id="1e1cb-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="1e1cb-839">Finance</span></span></td>
<td><span data-ttu-id="1e1cb-840">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-840">10001</span></span></td>
<td><span data-ttu-id="1e1cb-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-841">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-842">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="1e1cb-843">-8,150.29</span></span></td>
<td><span data-ttu-id="1e1cb-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-845">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-845">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-846">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-847">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-847">10001</span></span></td>
<td><span data-ttu-id="1e1cb-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-848">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-849">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1e1cb-850">5,297.69</span></span></td>
<td><span data-ttu-id="1e1cb-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-852">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-852">CC004</span></span></td>
<td><span data-ttu-id="1e1cb-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-853">Packaging</span></span></td>
<td><span data-ttu-id="1e1cb-854">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-854">10001</span></span></td>
<td><span data-ttu-id="1e1cb-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-855">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-856">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1e1cb-857">2,852.60</span></span></td>
<td><span data-ttu-id="1e1cb-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-859">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-859">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-860">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-861">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-861">10001</span></span></td>
<td><span data-ttu-id="1e1cb-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-862">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-863">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="1e1cb-864">-713.75</span></span></td>
<td><span data-ttu-id="1e1cb-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-866">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-867">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-868">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-868">10001</span></span></td>
<td><span data-ttu-id="1e1cb-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-869">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-870">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-871">535.31</span><span class="sxs-lookup"><span data-stu-id="1e1cb-871">535.31</span></span></td>
<td><span data-ttu-id="1e1cb-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-873">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-874">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-875">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-875">10001</span></span></td>
<td><span data-ttu-id="1e1cb-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-876">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-877">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-878">178.44</span><span class="sxs-lookup"><span data-stu-id="1e1cb-878">178.44</span></span></td>
<td><span data-ttu-id="1e1cb-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-880">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-880">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-881">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-882">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-882">10001</span></span></td>
<td><span data-ttu-id="1e1cb-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-883">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-884">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="1e1cb-885">-5,982.83</span></span></td>
<td><span data-ttu-id="1e1cb-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-887">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-888">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-889">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-889">10001</span></span></td>
<td><span data-ttu-id="1e1cb-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-890">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-891">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1e1cb-892">4,487.12</span></span></td>
<td><span data-ttu-id="1e1cb-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-894">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-895">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-896">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-896">10001</span></span></td>
<td><span data-ttu-id="1e1cb-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-897">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-898">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1e1cb-899">1,495.71</span></span></td>
<td><span data-ttu-id="1e1cb-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-901">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-901">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-902">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-903">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-903">10001</span></span></td>
<td><span data-ttu-id="1e1cb-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-904">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-905">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="1e1cb-906">-286.25</span></span></td>
<td><span data-ttu-id="1e1cb-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-908">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-909">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-910">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-910">10001</span></span></td>
<td><span data-ttu-id="1e1cb-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-911">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-912">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-913">241.05</span><span class="sxs-lookup"><span data-stu-id="1e1cb-913">241.05</span></span></td>
<td><span data-ttu-id="1e1cb-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-915">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-916">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-917">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-917">10001</span></span></td>
<td><span data-ttu-id="1e1cb-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-918">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-919">Fixed cost</span></span></td>
<td><span data-ttu-id="1e1cb-920">45.20</span><span class="sxs-lookup"><span data-stu-id="1e1cb-920">45.20</span></span></td>
<td><span data-ttu-id="1e1cb-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-922">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-922">CC003</span></span></td>
<td><span data-ttu-id="1e1cb-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="1e1cb-923">Assembly</span></span></td>
<td><span data-ttu-id="1e1cb-924">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-924">10001</span></span></td>
<td><span data-ttu-id="1e1cb-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-925">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-926">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="1e1cb-927">-2,977.17</span></span></td>
<td><span data-ttu-id="1e1cb-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-929">Prod 1</span></span></td>
<td><span data-ttu-id="1e1cb-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-930">Product 1</span></span></td>
<td><span data-ttu-id="1e1cb-931">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-931">10001</span></span></td>
<td><span data-ttu-id="1e1cb-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-932">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-933">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1e1cb-934">2,507.09</span></span></td>
<td><span data-ttu-id="1e1cb-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1e1cb-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-936">Prod 2</span></span></td>
<td><span data-ttu-id="1e1cb-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-937">Product 2</span></span></td>
<td><span data-ttu-id="1e1cb-938">10001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-938">10001</span></span></td>
<td><span data-ttu-id="1e1cb-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-939">Electricity</span></span></td>
<td><span data-ttu-id="1e1cb-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-940">Variable cost</span></span></td>
<td><span data-ttu-id="1e1cb-941">470.08</span><span class="sxs-lookup"><span data-stu-id="1e1cb-941">470.08</span></span></td>
<td><span data-ttu-id="1e1cb-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="1e1cb-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="1e1cb-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="1e1cb-943">Conclusion</span></span>
<span data-ttu-id="1e1cb-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="1e1cb-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="1e1cb-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="1e1cb-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="1e1cb-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="1e1cb-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="1e1cb-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="1e1cb-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="1e1cb-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1e1cb-951">CC099</span><span class="sxs-lookup"><span data-stu-id="1e1cb-951">CC099</span></span></th>
<th><span data-ttu-id="1e1cb-952">CC001</span><span class="sxs-lookup"><span data-stu-id="1e1cb-952">CC001</span></span></th>
<th><span data-ttu-id="1e1cb-953">CC002</span><span class="sxs-lookup"><span data-stu-id="1e1cb-953">CC002</span></span></th>
<th><span data-ttu-id="1e1cb-954">CC003</span><span class="sxs-lookup"><span data-stu-id="1e1cb-954">CC003</span></span></th>
<th><span data-ttu-id="1e1cb-955">CC004</span><span class="sxs-lookup"><span data-stu-id="1e1cb-955">CC004</span></span></th>
<th><span data-ttu-id="1e1cb-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-956">Proj 1</span></span></th>
<th><span data-ttu-id="1e1cb-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-957">Proj 2</span></span></th>
<th><span data-ttu-id="1e1cb-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="1e1cb-958">Prod 1</span></span></th>
<th><span data-ttu-id="1e1cb-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="1e1cb-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="1e1cb-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="1e1cb-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="1e1cb-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="1e1cb-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-971">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="1e1cb-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-973">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-974">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-975">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-976">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-977">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-978">776.36</span><span class="sxs-lookup"><span data-stu-id="1e1cb-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-979">223.64</span><span class="sxs-lookup"><span data-stu-id="1e1cb-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="1e1cb-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="1e1cb-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-982">000</span><span class="sxs-lookup"><span data-stu-id="1e1cb-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-983">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-984">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-985">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-986">0,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-987">30.00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-988">10,00</span><span class="sxs-lookup"><span data-stu-id="1e1cb-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1e1cb-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1e1cb-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1e1cb-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1e1cb-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e1cb-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="1e1cb-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="1e1cb-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="1e1cb-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="1e1cb-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="1e1cb-996">Дополнительные сведения см. в разделе [Свертка затрат](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="1e1cb-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



