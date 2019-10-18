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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179606"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4f8fc-103">Расчет накладных расходов</span><span class="sxs-lookup"><span data-stu-id="4f8fc-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f8fc-104">В этом разделе описываются типовые процессы расчета и распределения накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4f8fc-105">Определение термина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-105">Term definition</span></span>
---------------

<span data-ttu-id="4f8fc-106">Накладные расходы представляют собой затраты, понесенных с целью ведения бизнеса, которые, однако, нельзя отнести напрямую к какой-либо определенной деловой активности, продукту или услуге.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4f8fc-107">Накладные расходы предоставляют важную поддержку для создания действий, создающих прибыль.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4f8fc-108">Ниже приведены несколько примеров накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4f8fc-109">Аренда</span><span class="sxs-lookup"><span data-stu-id="4f8fc-109">Rent</span></span>
-   <span data-ttu-id="4f8fc-110">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-110">Electricity</span></span>
-   <span data-ttu-id="4f8fc-111">Заработная плата администрации</span><span class="sxs-lookup"><span data-stu-id="4f8fc-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4f8fc-112">Обзор расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="4f8fc-112">Overhead calculation overview</span></span>
<span data-ttu-id="4f8fc-113">Расчет накладных расходов применяет политики учета затрат в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4f8fc-114">Допускается выполнение расчета накладных расходов несколько раз для одного финансового периода, если были изменены политики учета затрат или обнаружены определенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4f8fc-115">Каждое выполнение расчета накладных расходов сохраняется и получает уникальный идентификатор версии, который позволяет сравнить расчеты в различных версиях.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4f8fc-116">Записи затрат, которые создает расчет накладных расходов, получают дату учета.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4f8fc-117">Эта дата учета соответствует дате окончания финансового периода, используемого в расчете.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4f8fc-118">Уникальный код версии состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="4f8fc-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4f8fc-119">Тип версии</span><span class="sxs-lookup"><span data-stu-id="4f8fc-119">Version type</span></span>
-   <span data-ttu-id="4f8fc-120">Дата и время</span><span class="sxs-lookup"><span data-stu-id="4f8fc-120">Date and time</span></span>
-   <span data-ttu-id="4f8fc-121">Книга учета затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4f8fc-122">Финансовый год</span><span class="sxs-lookup"><span data-stu-id="4f8fc-122">Fiscal year</span></span>
-   <span data-ttu-id="4f8fc-123">Учетный период</span><span class="sxs-lookup"><span data-stu-id="4f8fc-123">Fiscal period</span></span>

<span data-ttu-id="4f8fc-124">Расчет накладных расходов выполняется независимо от версии.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4f8fc-125">Таким образом можно рассчитать версию бюджета до фактической версии.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4f8fc-126">Расчет накладных расходов состоит из четырех этапов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4f8fc-127">На каждом этапе заголовок журнала будет создан с записями журнала.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4f8fc-128">Этот заголовок журнала отслеживает входные данные для каждого этапа вычисления.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4f8fc-129">Политики и правила применяются к каждой строке журнала, и записи затрат создаются на выходе.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4f8fc-130">Таким образом всегда имеется полное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4f8fc-131">[![Расчет накладных расходов](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4f8fc-132">Вычисление и распределение накладных расходов на электроэнергию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4f8fc-133">В финансовом учете некоторые затраты, например, за электричество, регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4f8fc-134">Таким образом, подробное представление для менеджеров не предоставляется для учета затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4f8fc-135">В учете затрат для представления правильных подробных данных для управления по всем подразделениям и уровням затраты должны проводиться через организационные подразделения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4f8fc-136">Этот поток должен основываться на точном учете потребления или на справедливой оценке.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4f8fc-137">В главной книге стоимость электроэнергии можно разносить, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-138">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-139">Центр затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-140">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="4f8fc-140">Main account</span></span></th>
<th><span data-ttu-id="4f8fc-141">Сумма в валюте учета</span><span class="sxs-lookup"><span data-stu-id="4f8fc-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-142">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-143">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-144">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-144">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-145">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-145">10001</span></span></td>
<td><span data-ttu-id="4f8fc-146">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-146">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4f8fc-148">Шаг 1: Обработка расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4f8fc-149">По умолчанию при импорте записей затрат из источника данных они получают классификацию поведения затрат **Неклассифицированные** в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4f8fc-150">Применяя правила политики поведение затрат, можно изменить классификацию записей затрат на **Постоянные затраты** или **Переменные затраты**.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4f8fc-151">Определения правила поведения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4f8fc-152">В некоторых случаях часть затрат являются фиксированным сбором, а оставшиеся затраты основаны на потреблении.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4f8fc-153">Счета за энергоснабжение часто соответствуют этому определению.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4f8fc-154">После оплаты определенного фиксированного сбор вы оплачиваете потребления за киловатт-час (кВт-ч).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4f8fc-155">Например, если сбор постоянных затрат равен 1 000,00, правило поведения затрат определяется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4f8fc-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4f8fc-156">Фиксированная сумма 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4f8fc-157">0 &lt;= 1 000,00 = Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4f8fc-158">1000,01 &lt; N = Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4f8fc-159">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-160">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-160">Journal</span></span></th>
<th><span data-ttu-id="4f8fc-161">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="4f8fc-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4f8fc-162">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="4f8fc-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4f8fc-163">Версия</span><span class="sxs-lookup"><span data-stu-id="4f8fc-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-164">00001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-164">00001</span></span></td>
<td><span data-ttu-id="4f8fc-165">Журнал расчета поведения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4f8fc-166">Финансовый</span><span class="sxs-lookup"><span data-stu-id="4f8fc-166">Fiscal</span></span></td>
<td><span data-ttu-id="4f8fc-167">2017</span><span class="sxs-lookup"><span data-stu-id="4f8fc-167">2017</span></span></td>
<td><span data-ttu-id="4f8fc-168">Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-168">Period 1</span></span></td>
<td><span data-ttu-id="4f8fc-169">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4f8fc-170">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-171">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-172">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-173">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-173">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-174">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-175">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-176">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-177">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-178">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-178">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-179">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-179">10001</span></span></td>
<td><span data-ttu-id="4f8fc-180">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-180">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-181">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="4f8fc-181">Unclassified</span></span></td>
<td><span data-ttu-id="4f8fc-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4f8fc-183">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-184">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-185">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-185">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-186">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-187">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-187">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-188">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-189">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-190">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-190">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-191">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-191">10001</span></span></td>
<td><span data-ttu-id="4f8fc-192">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-192">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-193">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="4f8fc-193">Unclassified</span></span></td>
<td><span data-ttu-id="4f8fc-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-194">10,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-195">3 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-196">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-197">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-197">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-198">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-198">10001</span></span></td>
<td><span data-ttu-id="4f8fc-199">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-199">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-200">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="4f8fc-200">Unclassified</span></span></td>
<td><span data-ttu-id="4f8fc-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-202">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-203">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-204">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-204">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-205">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-205">10001</span></span></td>
<td><span data-ttu-id="4f8fc-206">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-206">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-207">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-208">1,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-209">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-210">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-211">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-211">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-212">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-212">10001</span></span></td>
<td><span data-ttu-id="4f8fc-213">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-213">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-214">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-214">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-215">9,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-216">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-217">Дополнительные сведения см. в разделе [Создание политик поведения затрат и их назначение единицам управления затратами](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4f8fc-218">Шаг 2: Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4f8fc-219">Распределение затрат используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4f8fc-220">Распределение затрат и назначение затрат отличаются тем, что распределение затрат всегда происходит на уровне первичного элемента затрат исходных затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4f8fc-221">Определение правила распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4f8fc-222">В финансовом учете затраты на электричество часто регистрируются как общая сумма.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4f8fc-223">В учете затрат такой подход недостаточно детализирован.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4f8fc-224">Переменные затраты должны распределяться по индивидуальным объектам затрат на справедливой основе.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4f8fc-225">Наиболее логичной основой распределения является потребление энергии (киловатт-час).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4f8fc-226">Создается элемент статистической аналитики с названием "Электричество", и записывается потребление энергии.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4f8fc-227">По умолчанию все элементы статистической аналитики становятся доступными как основа распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-228">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-228">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-229">кВт-ч</span><span class="sxs-lookup"><span data-stu-id="4f8fc-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-230">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-231">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-231">HR</span></span></td>
<td><span data-ttu-id="4f8fc-232">1000</span><span class="sxs-lookup"><span data-stu-id="4f8fc-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-233">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-234">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-234">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4f8fc-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-236">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-237">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-237">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-238">0</span><span class="sxs-lookup"><span data-stu-id="4f8fc-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-239">Следующая таблица показывает результат при применении потребления энергии как основы для распределения переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-240">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-240">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-241">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-241">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-242">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-243">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-244">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-245">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-245">HR</span></span></td>
<td><span data-ttu-id="4f8fc-246">1000</span><span class="sxs-lookup"><span data-stu-id="4f8fc-246">1,000</span></span></td>
<td><span data-ttu-id="4f8fc-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-249">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-250">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-250">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4f8fc-251">6,000</span></span></td>
<td><span data-ttu-id="4f8fc-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4f8fc-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-254">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-255">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-255">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-256">0</span><span class="sxs-lookup"><span data-stu-id="4f8fc-256">0</span></span></td>
<td><span data-ttu-id="4f8fc-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-259">Фиксированные затраты должны распределяться поровну между отдельными объектами, которые потребляют электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4f8fc-260">Этого результата можно добиться с помощью элемента статистической аналитики "Электричество" в формуле базы распределения: (Электричество &gt; 0,00) В следующей таблице показан результат, когда потребление электроэнергии применяется в качестве основы распределения для переменных затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-261">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-261">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-262">Формула</span><span class="sxs-lookup"><span data-stu-id="4f8fc-262">Formula</span></span></th>
<th><span data-ttu-id="4f8fc-263">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-263">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-264">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-265">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-266">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-267">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-267">HR</span></span></td>
<td><span data-ttu-id="4f8fc-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4f8fc-269">1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-269">1</span></span></td>
<td><span data-ttu-id="4f8fc-270">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-271">500.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-272">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-273">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-273">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4f8fc-275">1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-275">1</span></span></td>
<td><span data-ttu-id="4f8fc-276">(1 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-277">500.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-278">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-279">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-279">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4f8fc-281">0</span><span class="sxs-lookup"><span data-stu-id="4f8fc-281">0</span></span></td>
<td><span data-ttu-id="4f8fc-282">(0 ÷ 2) × 1000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4f8fc-284">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-285">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-285">Journal</span></span></th>
<th><span data-ttu-id="4f8fc-286">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="4f8fc-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4f8fc-287">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="4f8fc-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4f8fc-288">Версия</span><span class="sxs-lookup"><span data-stu-id="4f8fc-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-289">00002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-289">00002</span></span></td>
<td><span data-ttu-id="4f8fc-290">Журнал расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4f8fc-291">Финансовый</span><span class="sxs-lookup"><span data-stu-id="4f8fc-291">Fiscal</span></span></td>
<td><span data-ttu-id="4f8fc-292">2017</span><span class="sxs-lookup"><span data-stu-id="4f8fc-292">2017</span></span></td>
<td><span data-ttu-id="4f8fc-293">Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-293">Period 1</span></span></td>
<td><span data-ttu-id="4f8fc-294">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4f8fc-295">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-296">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-297">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-298">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-298">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-299">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-300">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-301">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-302">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-303">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-303">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-304">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-304">10001</span></span></td>
<td><span data-ttu-id="4f8fc-305">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-305">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-306">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-308">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-309">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-310">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-310">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-311">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-311">10001</span></span></td>
<td><span data-ttu-id="4f8fc-312">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-312">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-313">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-313">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4f8fc-315">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-316">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-317">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-317">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-318">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-319">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-319">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-320">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-321">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-322">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-322">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-323">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-323">10001</span></span></td>
<td><span data-ttu-id="4f8fc-324">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-324">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-325">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-327">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-328">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-329">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-329">HR</span></span></td>
<td><span data-ttu-id="4f8fc-330">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-330">10001</span></span></td>
<td><span data-ttu-id="4f8fc-331">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-331">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-332">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-333">500.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-333">500.00</span></span></td>
<td><span data-ttu-id="4f8fc-334">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-335">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-336">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-336">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-337">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-337">10001</span></span></td>
<td><span data-ttu-id="4f8fc-338">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-338">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-339">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-340">500.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-340">500.00</span></span></td>
<td><span data-ttu-id="4f8fc-341">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-342">CC099</span></span></td>
<td><span data-ttu-id="4f8fc-343">Центр затрат по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4f8fc-343">Default cost center</span></span></td>
<td><span data-ttu-id="4f8fc-344">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-344">10001</span></span></td>
<td><span data-ttu-id="4f8fc-345">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-345">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-346">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-346">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-347">-9000,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4f8fc-348">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-349">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-350">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-350">HR</span></span></td>
<td><span data-ttu-id="4f8fc-351">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-351">10001</span></span></td>
<td><span data-ttu-id="4f8fc-352">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-352">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-353">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-353">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-354">1,285.71</span></span></td>
<td><span data-ttu-id="4f8fc-355">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-356">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-357">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-357">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-358">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-358">10001</span></span></td>
<td><span data-ttu-id="4f8fc-359">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-359">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-360">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-360">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4f8fc-361">7,714.29</span></span></td>
<td><span data-ttu-id="4f8fc-362">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-363">Дополнительные сведения см. в разделе [Создание политики распределения затрат и назначение ее единице управления затратами](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4f8fc-364">Шаг 3. Обработка расчета ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="4f8fc-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4f8fc-365">Ставка накладных расходов используется для отнесения затрат на один или несколько конкретных объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4f8fc-366">Затраты основаны на предопределенной норме затрат и величине от назначенной базы распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4f8fc-367">Определение ставки накладных расходов</span><span class="sxs-lookup"><span data-stu-id="4f8fc-367">Define the overhead rate</span></span>

<span data-ttu-id="4f8fc-368">Объект затрат "CC001 Отдел кадров" вносит вклад в ряд внутренних проектов.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4f8fc-369">Элемент статистической аналитики с именем "Проекты отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-370">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-370">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-371">Часы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-372">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-372">Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-373">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-373">Project 1</span></span></td>
<td><span data-ttu-id="4f8fc-374">3</span><span class="sxs-lookup"><span data-stu-id="4f8fc-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-375">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-375">Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-376">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-376">Project 2</span></span></td>
<td><span data-ttu-id="4f8fc-377">1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-378">Была определена предопределенная норма затрат для вклада проектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-379">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-379">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-380">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-380">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-381">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-382">Единицы измерения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-382">Units</span></span></th>
<th><span data-ttu-id="4f8fc-383">По норме</span><span class="sxs-lookup"><span data-stu-id="4f8fc-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-384">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-385">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-385">HR</span></span></td>
<td><span data-ttu-id="4f8fc-386">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-386">10001</span></span></td>
<td><span data-ttu-id="4f8fc-387">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-387">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-388">1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-388">1</span></span></td>
<td><span data-ttu-id="4f8fc-389">10</span><span class="sxs-lookup"><span data-stu-id="4f8fc-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-390">В следующей таблице показаны результаты при применении проектов отдела кадров в качестве базы для распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-391">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-391">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-392">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-392">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-393">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-393">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-394">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-395">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-396">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-396">Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-397">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-397">Project 1</span></span></td>
<td><span data-ttu-id="4f8fc-398">3</span><span class="sxs-lookup"><span data-stu-id="4f8fc-398">3</span></span></td>
<td><span data-ttu-id="4f8fc-399">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-399">10001</span></span></td>
<td><span data-ttu-id="4f8fc-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4f8fc-401">30.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-402">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-402">Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-403">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-403">Project 2</span></span></td>
<td><span data-ttu-id="4f8fc-404">1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-404">1</span></span></td>
<td><span data-ttu-id="4f8fc-405">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-405">10001</span></span></td>
<td><span data-ttu-id="4f8fc-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4f8fc-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4f8fc-408">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-409">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-409">Journal</span></span></th>
<th><span data-ttu-id="4f8fc-410">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="4f8fc-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4f8fc-411">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="4f8fc-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4f8fc-412">Версия</span><span class="sxs-lookup"><span data-stu-id="4f8fc-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-413">00003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-413">00003</span></span></td>
<td><span data-ttu-id="4f8fc-414">Журнал расчета накладных расходов</span><span class="sxs-lookup"><span data-stu-id="4f8fc-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4f8fc-415">Финансовый</span><span class="sxs-lookup"><span data-stu-id="4f8fc-415">Fiscal</span></span></td>
<td><span data-ttu-id="4f8fc-416">2017</span><span class="sxs-lookup"><span data-stu-id="4f8fc-416">2017</span></span></td>
<td><span data-ttu-id="4f8fc-417">Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-417">Period 1</span></span></td>
<td><span data-ttu-id="4f8fc-418">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4f8fc-419">Записи журнала (записи журнала для расчета накладных расходов)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-420">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-421">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-421">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-422">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-423">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-424">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-424">Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-425">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-427">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-428">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-428">Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-429">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-430">1.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4f8fc-431">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-432">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-433">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-433">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-434">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-435">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-435">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-436">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-437">CC0001</span></span></td>
<td><span data-ttu-id="4f8fc-438">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-438">HR</span></span></td>
<td><span data-ttu-id="4f8fc-439">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-439">10001</span></span></td>
<td><span data-ttu-id="4f8fc-440">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-440">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-441">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-441">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-442">-30.00</span></span></td>
<td><span data-ttu-id="4f8fc-443">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-444">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-444">Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-445">Внутренний проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4f8fc-446">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-446">10001</span></span></td>
<td><span data-ttu-id="4f8fc-447">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-447">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-448">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-448">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-449">30.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-449">30.00</span></span></td>
<td><span data-ttu-id="4f8fc-450">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-451">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-452">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-452">HR</span></span></td>
<td><span data-ttu-id="4f8fc-453">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-453">10001</span></span></td>
<td><span data-ttu-id="4f8fc-454">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-454">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-455">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-455">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-456">-10.00</span></span></td>
<td><span data-ttu-id="4f8fc-457">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-458">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-458">Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-459">Внутренний проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4f8fc-460">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-460">10001</span></span></td>
<td><span data-ttu-id="4f8fc-461">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-461">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-462">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-462">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-463">10.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-463">10.00</span></span></td>
<td><span data-ttu-id="4f8fc-464">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-465">Дополнительные сведения см. в разделе [Выполнение расчета накладных расходов](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4f8fc-466">Шаг 4. Обработка расчета распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4f8fc-467">Распределение используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4f8fc-468">Finance поддерживает метод взаимного распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4f8fc-469">В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4f8fc-470">Система автоматически определяет правильный порядок, в котором требуется выполнять распределение.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4f8fc-471">Сальдо объекта затрат распределяется одной базой распределения.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4f8fc-472">Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4f8fc-473">Порядок распределения управляется единицей управления затратами.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4f8fc-474">[![Взаимный метод](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4f8fc-475">Определение распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-475">Define the cost allocation</span></span>

<span data-ttu-id="4f8fc-476">Вот простой пример, объясняющий, как можно отслеживать движение затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4f8fc-477">Объект затрат "CC001 Отдел кадров" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4f8fc-478">Элемент статистической аналитики с именем "Услуги отдела кадров" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-479">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-479">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-480">Услуги отдела кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-481">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-482">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-482">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-483">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-484">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-485">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-485">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-486">55</span><span class="sxs-lookup"><span data-stu-id="4f8fc-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-487">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-488">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-488">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-489">10</span><span class="sxs-lookup"><span data-stu-id="4f8fc-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-490">Объект затрат "CC002 Финансовый отдел" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4f8fc-491">Элемент статистической аналитики с именем "Услуги финансового отдела" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-492">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-492">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-493">Услуги финансового отдела</span><span class="sxs-lookup"><span data-stu-id="4f8fc-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-494">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-495">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-495">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-496">65</span><span class="sxs-lookup"><span data-stu-id="4f8fc-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-497">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-498">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-498">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-499">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-500">Объект затрат "CC003 Сборка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4f8fc-501">Элемент статистической аналитики с именем "Услуги сборки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-502">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-502">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-503">Услуги сборки (в часах)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-504">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-504">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-505">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-505">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-506">60</span><span class="sxs-lookup"><span data-stu-id="4f8fc-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-507">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-507">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-508">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-508">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-509">20</span><span class="sxs-lookup"><span data-stu-id="4f8fc-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-510">Объект затрат "CC004 Упаковка" вносит вклад в несколько объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4f8fc-511">Элемент статистической аналитики с именем "Услуги упаковки" создается для измерения потребленной величины.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-512">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-512">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-513">Услуги упаковки (в часах)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-514">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-514">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-515">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-515">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-516">80</span><span class="sxs-lookup"><span data-stu-id="4f8fc-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-517">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-517">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-518">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-518">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-519">15</span><span class="sxs-lookup"><span data-stu-id="4f8fc-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4f8fc-520">Статистические меры, такие как время производства, потребляемое продуктом, могут быть получены из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4f8fc-521">Дополнительные сведения см. в разделе [Шаблон поставщика статистической меры](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4f8fc-522">В следующей таблице показан результат, когда услуги HR-отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-523">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-523">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-524">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-524">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-525">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-526">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-526">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-527">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-528">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-529">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-529">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-530">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-530">35</span></span></td>
<td><span data-ttu-id="4f8fc-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4f8fc-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-532">175.00</span></span></td>
<td><span data-ttu-id="4f8fc-533">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-534">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-535">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-535">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-536">55</span><span class="sxs-lookup"><span data-stu-id="4f8fc-536">55</span></span></td>
<td><span data-ttu-id="4f8fc-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4f8fc-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-538">275.00</span></span></td>
<td><span data-ttu-id="4f8fc-539">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-540">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-541">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-541">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-542">10</span><span class="sxs-lookup"><span data-stu-id="4f8fc-542">10</span></span></td>
<td><span data-ttu-id="4f8fc-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4f8fc-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-544">50.00</span></span></td>
<td><span data-ttu-id="4f8fc-545">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-546">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-547">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-547">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-548">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-548">35</span></span></td>
<td><span data-ttu-id="4f8fc-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4f8fc-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-550">436.00</span></span></td>
<td><span data-ttu-id="4f8fc-551">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-552">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-553">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-553">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-554">55</span><span class="sxs-lookup"><span data-stu-id="4f8fc-554">55</span></span></td>
<td><span data-ttu-id="4f8fc-555">(55 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4f8fc-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4f8fc-556">685.14</span></span></td>
<td><span data-ttu-id="4f8fc-557">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-558">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-559">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-559">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-560">10</span><span class="sxs-lookup"><span data-stu-id="4f8fc-560">10</span></span></td>
<td><span data-ttu-id="4f8fc-561">(10 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4f8fc-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4f8fc-562">124.57</span></span></td>
<td><span data-ttu-id="4f8fc-563">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-564">В следующей таблице показан результат, когда услуги финансового отдела применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-565">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-565">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-566">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-566">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-567">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-568">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-568">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-569">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-570">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-571">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-571">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-572">65</span><span class="sxs-lookup"><span data-stu-id="4f8fc-572">65</span></span></td>
<td><span data-ttu-id="4f8fc-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4f8fc-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4f8fc-574">438.75</span></span></td>
<td><span data-ttu-id="4f8fc-575">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-576">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-577">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-577">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-578">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-578">35</span></span></td>
<td><span data-ttu-id="4f8fc-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4f8fc-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4f8fc-580">236.25</span></span></td>
<td><span data-ttu-id="4f8fc-581">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-582">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-583">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-583">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-584">65</span><span class="sxs-lookup"><span data-stu-id="4f8fc-584">65</span></span></td>
<td><span data-ttu-id="4f8fc-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4f8fc-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4f8fc-586">5,297.69</span></span></td>
<td><span data-ttu-id="4f8fc-587">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-588">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-589">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-589">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-590">35</span><span class="sxs-lookup"><span data-stu-id="4f8fc-590">35</span></span></td>
<td><span data-ttu-id="4f8fc-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4f8fc-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4f8fc-592">2,852.60</span></span></td>
<td><span data-ttu-id="4f8fc-593">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-594">В следующей таблице показан результат, когда услуги сборки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-595">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-595">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-596">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-596">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-597">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-598">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-598">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-599">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-600">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-600">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-601">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-601">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-602">60</span><span class="sxs-lookup"><span data-stu-id="4f8fc-602">60</span></span></td>
<td><span data-ttu-id="4f8fc-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4f8fc-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4f8fc-604">535.31</span></span></td>
<td><span data-ttu-id="4f8fc-605">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-606">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-606">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-607">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-607">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-608">20</span><span class="sxs-lookup"><span data-stu-id="4f8fc-608">20</span></span></td>
<td><span data-ttu-id="4f8fc-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4f8fc-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4f8fc-610">178.44</span></span></td>
<td><span data-ttu-id="4f8fc-611">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-612">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-612">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-613">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-613">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-614">60</span><span class="sxs-lookup"><span data-stu-id="4f8fc-614">60</span></span></td>
<td><span data-ttu-id="4f8fc-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4f8fc-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4f8fc-616">4,487.12</span></span></td>
<td><span data-ttu-id="4f8fc-617">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-618">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-618">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-619">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-619">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-620">20</span><span class="sxs-lookup"><span data-stu-id="4f8fc-620">20</span></span></td>
<td><span data-ttu-id="4f8fc-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4f8fc-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-622">1,495.71</span></span></td>
<td><span data-ttu-id="4f8fc-623">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f8fc-624">В следующей таблице показан результат, когда услуги упаковки применяются как база распределения общих затрат (фиксированные затраты и переменные затраты).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-625">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-625">Cost object</span></span></th>
<th><span data-ttu-id="4f8fc-626">Величина</span><span class="sxs-lookup"><span data-stu-id="4f8fc-626">Magnitude</span></span></th>
<th><span data-ttu-id="4f8fc-627">Коэффициент распределения</span><span class="sxs-lookup"><span data-stu-id="4f8fc-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4f8fc-628">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-628">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-629">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-630">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-630">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-631">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-631">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-632">80</span><span class="sxs-lookup"><span data-stu-id="4f8fc-632">80</span></span></td>
<td><span data-ttu-id="4f8fc-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4f8fc-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4f8fc-634">241.05</span></span></td>
<td><span data-ttu-id="4f8fc-635">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-636">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-636">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-637">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-637">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-638">15</span><span class="sxs-lookup"><span data-stu-id="4f8fc-638">15</span></span></td>
<td><span data-ttu-id="4f8fc-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4f8fc-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4f8fc-640">45.20</span></span></td>
<td><span data-ttu-id="4f8fc-641">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-642">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-642">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-643">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-643">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-644">80</span><span class="sxs-lookup"><span data-stu-id="4f8fc-644">80</span></span></td>
<td><span data-ttu-id="4f8fc-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4f8fc-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4f8fc-646">2,507.09</span></span></td>
<td><span data-ttu-id="4f8fc-647">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-648">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-648">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-649">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-649">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-650">15</span><span class="sxs-lookup"><span data-stu-id="4f8fc-650">15</span></span></td>
<td><span data-ttu-id="4f8fc-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4f8fc-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4f8fc-652">470.08</span></span></td>
<td><span data-ttu-id="4f8fc-653">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4f8fc-654">Записи в журнале (записи журнала для сальдо объекта затрат)</span><span class="sxs-lookup"><span data-stu-id="4f8fc-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-655">Журнал</span><span class="sxs-lookup"><span data-stu-id="4f8fc-655">Journal</span></span></th>
<th><span data-ttu-id="4f8fc-656">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="4f8fc-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4f8fc-657">Период финансового календаря</span><span class="sxs-lookup"><span data-stu-id="4f8fc-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4f8fc-658">Версия</span><span class="sxs-lookup"><span data-stu-id="4f8fc-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-659">00004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-659">00004</span></span></td>
<td><span data-ttu-id="4f8fc-660">Журнал распределения затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4f8fc-661">Финансовый</span><span class="sxs-lookup"><span data-stu-id="4f8fc-661">Fiscal</span></span></td>
<td><span data-ttu-id="4f8fc-662">2017</span><span class="sxs-lookup"><span data-stu-id="4f8fc-662">2017</span></span></td>
<td><span data-ttu-id="4f8fc-663">Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-663">Period 1</span></span></td>
<td><span data-ttu-id="4f8fc-664">Расчет накладных расходов / 01-02-2017 23:51:00 / ГК / 2017 / Период 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4f8fc-665">Строки журнала</span><span class="sxs-lookup"><span data-stu-id="4f8fc-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4f8fc-666">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-667">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-668">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-668">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-669">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-670">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-671">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-672">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-673">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-673">HR</span></span></td>
<td><span data-ttu-id="4f8fc-674">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-674">10001</span></span></td>
<td><span data-ttu-id="4f8fc-675">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-675">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-676">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-677">500.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-678">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-679">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-680">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-680">HR</span></span></td>
<td><span data-ttu-id="4f8fc-681">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-681">10001</span></span></td>
<td><span data-ttu-id="4f8fc-682">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-682">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-683">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-683">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-685">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-686">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-687">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-687">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-688">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-688">10001</span></span></td>
<td><span data-ttu-id="4f8fc-689">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-689">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-690">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-692">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-693">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-694">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-694">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-695">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-695">10001</span></span></td>
<td><span data-ttu-id="4f8fc-696">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-696">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-697">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-697">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4f8fc-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-699">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-700">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-701">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-701">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-702">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-702">10001</span></span></td>
<td><span data-ttu-id="4f8fc-703">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-703">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-704">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4f8fc-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-706">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-707">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-708">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-708">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-709">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-709">10001</span></span></td>
<td><span data-ttu-id="4f8fc-710">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-710">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-711">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-711">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4f8fc-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-713">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-714">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-715">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-715">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-716">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-716">10001</span></span></td>
<td><span data-ttu-id="4f8fc-717">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-717">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-718">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4f8fc-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-720">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-721">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-722">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-722">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-723">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-723">10001</span></span></td>
<td><span data-ttu-id="4f8fc-724">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-724">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-725">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-725">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4f8fc-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-727">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-728">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-728">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-729">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-729">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-730">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-730">10001</span></span></td>
<td><span data-ttu-id="4f8fc-731">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-731">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-732">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4f8fc-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-734">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-735">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-735">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-736">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-736">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-737">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-737">10001</span></span></td>
<td><span data-ttu-id="4f8fc-738">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-738">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-739">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-739">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4f8fc-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-741">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-742">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-742">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-743">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-743">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-744">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-744">10001</span></span></td>
<td><span data-ttu-id="4f8fc-745">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-745">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-746">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4f8fc-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-748">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4f8fc-749">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-749">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-750">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-750">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-751">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-751">10001</span></span></td>
<td><span data-ttu-id="4f8fc-752">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-752">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-753">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-753">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4f8fc-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4f8fc-755">Записи затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4f8fc-756">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4f8fc-757">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-757">Cost element</span></span></th>
<th><span data-ttu-id="4f8fc-758">Поведение затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4f8fc-759">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-759">Amount</span></span></th>
<th><span data-ttu-id="4f8fc-760">Финансовая дата</span><span class="sxs-lookup"><span data-stu-id="4f8fc-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4f8fc-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-761">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-762">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-762">HR</span></span></td>
<td><span data-ttu-id="4f8fc-763">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-763">10001</span></span></td>
<td><span data-ttu-id="4f8fc-764">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-764">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-765">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-766">-500.00</span></span></td>
<td><span data-ttu-id="4f8fc-767">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-768">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-769">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-769">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-770">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-770">10001</span></span></td>
<td><span data-ttu-id="4f8fc-771">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-771">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-772">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-773">175.00</span></span></td>
<td><span data-ttu-id="4f8fc-774">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-775">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-776">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-776">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-777">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-777">10001</span></span></td>
<td><span data-ttu-id="4f8fc-778">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-778">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-779">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-780">275.00</span></span></td>
<td><span data-ttu-id="4f8fc-781">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-782">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-783">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-783">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-784">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-784">10001</span></span></td>
<td><span data-ttu-id="4f8fc-785">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-785">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-786">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-787">50,00</span></span></td>
<td><span data-ttu-id="4f8fc-788">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-789">CC001</span></span></td>
<td><span data-ttu-id="4f8fc-790">Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4f8fc-790">HR</span></span></td>
<td><span data-ttu-id="4f8fc-791">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-791">10001</span></span></td>
<td><span data-ttu-id="4f8fc-792">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-792">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-793">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-793">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-794">-1245,71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4f8fc-795">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-796">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-797">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-797">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-798">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-798">10001</span></span></td>
<td><span data-ttu-id="4f8fc-799">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-799">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-800">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-800">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-801">436.00</span></span></td>
<td><span data-ttu-id="4f8fc-802">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-803">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-804">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-804">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-805">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-805">10001</span></span></td>
<td><span data-ttu-id="4f8fc-806">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-806">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-807">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-807">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4f8fc-808">685.14</span></span></td>
<td><span data-ttu-id="4f8fc-809">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-810">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-811">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-811">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-812">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-812">10001</span></span></td>
<td><span data-ttu-id="4f8fc-813">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-813">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-814">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-814">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4f8fc-815">124.57</span></span></td>
<td><span data-ttu-id="4f8fc-816">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-817">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-818">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-818">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-819">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-819">10001</span></span></td>
<td><span data-ttu-id="4f8fc-820">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-820">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-821">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-822">-675.00</span></span></td>
<td><span data-ttu-id="4f8fc-823">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-824">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-825">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-825">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-826">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-826">10001</span></span></td>
<td><span data-ttu-id="4f8fc-827">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-827">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-828">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4f8fc-829">438.75</span></span></td>
<td><span data-ttu-id="4f8fc-830">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-831">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-832">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-832">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-833">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-833">10001</span></span></td>
<td><span data-ttu-id="4f8fc-834">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-834">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-835">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4f8fc-836">236.25</span></span></td>
<td><span data-ttu-id="4f8fc-837">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-838">CC002</span></span></td>
<td><span data-ttu-id="4f8fc-839">Финансы</span><span class="sxs-lookup"><span data-stu-id="4f8fc-839">Finance</span></span></td>
<td><span data-ttu-id="4f8fc-840">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-840">10001</span></span></td>
<td><span data-ttu-id="4f8fc-841">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-841">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-842">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-842">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-843">-8150,29</span><span class="sxs-lookup"><span data-stu-id="4f8fc-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4f8fc-844">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-845">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-846">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-846">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-847">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-847">10001</span></span></td>
<td><span data-ttu-id="4f8fc-848">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-848">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-849">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-849">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4f8fc-850">5,297.69</span></span></td>
<td><span data-ttu-id="4f8fc-851">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-852">CC004</span></span></td>
<td><span data-ttu-id="4f8fc-853">Упаковка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-853">Packaging</span></span></td>
<td><span data-ttu-id="4f8fc-854">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-854">10001</span></span></td>
<td><span data-ttu-id="4f8fc-855">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-855">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-856">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-856">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4f8fc-857">2,852.60</span></span></td>
<td><span data-ttu-id="4f8fc-858">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-859">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-860">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-860">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-861">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-861">10001</span></span></td>
<td><span data-ttu-id="4f8fc-862">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-862">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-863">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="4f8fc-864">-713.75</span></span></td>
<td><span data-ttu-id="4f8fc-865">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-866">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-866">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-867">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-867">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-868">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-868">10001</span></span></td>
<td><span data-ttu-id="4f8fc-869">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-869">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-870">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4f8fc-871">535.31</span></span></td>
<td><span data-ttu-id="4f8fc-872">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-873">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-873">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-874">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-874">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-875">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-875">10001</span></span></td>
<td><span data-ttu-id="4f8fc-876">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-876">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-877">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4f8fc-878">178.44</span></span></td>
<td><span data-ttu-id="4f8fc-879">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-880">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-881">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-881">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-882">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-882">10001</span></span></td>
<td><span data-ttu-id="4f8fc-883">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-883">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-884">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-884">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-885">-5982,83</span><span class="sxs-lookup"><span data-stu-id="4f8fc-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4f8fc-886">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-887">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-887">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-888">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-888">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-889">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-889">10001</span></span></td>
<td><span data-ttu-id="4f8fc-890">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-890">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-891">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-891">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4f8fc-892">4,487.12</span></span></td>
<td><span data-ttu-id="4f8fc-893">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-894">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-894">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-895">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-895">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-896">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-896">10001</span></span></td>
<td><span data-ttu-id="4f8fc-897">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-897">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-898">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-898">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4f8fc-899">1,495.71</span></span></td>
<td><span data-ttu-id="4f8fc-900">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-901">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-902">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-902">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-903">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-903">10001</span></span></td>
<td><span data-ttu-id="4f8fc-904">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-904">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-905">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="4f8fc-906">-286.25</span></span></td>
<td><span data-ttu-id="4f8fc-907">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-908">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-908">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-909">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-909">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-910">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-910">10001</span></span></td>
<td><span data-ttu-id="4f8fc-911">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-911">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-912">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4f8fc-913">241.05</span></span></td>
<td><span data-ttu-id="4f8fc-914">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-915">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-915">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-916">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-916">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-917">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-917">10001</span></span></td>
<td><span data-ttu-id="4f8fc-918">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-918">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-919">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4f8fc-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4f8fc-920">45.20</span></span></td>
<td><span data-ttu-id="4f8fc-921">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-922">CC003</span></span></td>
<td><span data-ttu-id="4f8fc-923">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f8fc-923">Assembly</span></span></td>
<td><span data-ttu-id="4f8fc-924">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-924">10001</span></span></td>
<td><span data-ttu-id="4f8fc-925">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-925">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-926">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-926">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="4f8fc-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4f8fc-928">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-929">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-929">Prod 1</span></span></td>
<td><span data-ttu-id="4f8fc-930">Продукт 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-930">Product 1</span></span></td>
<td><span data-ttu-id="4f8fc-931">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-931">10001</span></span></td>
<td><span data-ttu-id="4f8fc-932">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-932">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-933">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-933">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4f8fc-934">2,507.09</span></span></td>
<td><span data-ttu-id="4f8fc-935">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4f8fc-936">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-936">Prod 2</span></span></td>
<td><span data-ttu-id="4f8fc-937">Продукт 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-937">Product 2</span></span></td>
<td><span data-ttu-id="4f8fc-938">10001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-938">10001</span></span></td>
<td><span data-ttu-id="4f8fc-939">Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-939">Electricity</span></span></td>
<td><span data-ttu-id="4f8fc-940">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-940">Variable cost</span></span></td>
<td><span data-ttu-id="4f8fc-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4f8fc-941">470.08</span></span></td>
<td><span data-ttu-id="4f8fc-942">31 января 2017 года</span><span class="sxs-lookup"><span data-stu-id="4f8fc-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4f8fc-943">Заключение</span><span class="sxs-lookup"><span data-stu-id="4f8fc-943">Conclusion</span></span>
<span data-ttu-id="4f8fc-944">В финансовом учете затраты 10 000,00 за электричество разносятся на фиктивный код центра затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4f8fc-945">Таким образом бухгалтеры затрат будет знать, что эти затраты должны быть распределены.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4f8fc-946">В учете затрат затраты проходят через организационные подразделения и уровни на основе политик и правил, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4f8fc-947">Каждая затрата была связана с базой затрат, которая обеспечивает лучшую оценку для распределения затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4f8fc-948">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4f8fc-949">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="4f8fc-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4f8fc-950">Итоговый</span><span class="sxs-lookup"><span data-stu-id="4f8fc-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4f8fc-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4f8fc-951">CC099</span></span></th>
<th><span data-ttu-id="4f8fc-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4f8fc-952">CC001</span></span></th>
<th><span data-ttu-id="4f8fc-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4f8fc-953">CC002</span></span></th>
<th><span data-ttu-id="4f8fc-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4f8fc-954">CC003</span></span></th>
<th><span data-ttu-id="4f8fc-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4f8fc-955">CC004</span></span></th>
<th><span data-ttu-id="4f8fc-956">Проект 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-956">Proj 1</span></span></th>
<th><span data-ttu-id="4f8fc-957">Проект 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-957">Proj 2</span></span></th>
<th><span data-ttu-id="4f8fc-958">Прод. 1</span><span class="sxs-lookup"><span data-stu-id="4f8fc-958">Prod 1</span></span></th>
<th><span data-ttu-id="4f8fc-959">Прод. 2</span><span class="sxs-lookup"><span data-stu-id="4f8fc-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4f8fc-960">10001 Электричество</span><span class="sxs-lookup"><span data-stu-id="4f8fc-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4f8fc-970">Неклассифицированные</span><span class="sxs-lookup"><span data-stu-id="4f8fc-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4f8fc-972">Постоянные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4f8fc-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4f8fc-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4f8fc-981">Переменные затраты</span><span class="sxs-lookup"><span data-stu-id="4f8fc-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-982">000</span><span class="sxs-lookup"><span data-stu-id="4f8fc-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-987">30.00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4f8fc-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4f8fc-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4f8fc-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4f8fc-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4f8fc-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4f8fc-992">В этом разделе показано, как основной элемент затрат, 10001 Электричество, проходит через объекты затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4f8fc-993">Таким образом, стоимость этих накладных расходов распределяется на самые нижние уровни в организации.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4f8fc-994">Другими словами, объекты затрат на самом нижнем уровне используются для покрытия затрат.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4f8fc-995">Если требуется визуальное представление потока затрат между объектами затрат, можно использовать правила политики свертки затрат для визуализации потока по затратам.</span><span class="sxs-lookup"><span data-stu-id="4f8fc-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4f8fc-996">Дополнительные сведения см. в разделе [Свертка затрат](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="4f8fc-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



