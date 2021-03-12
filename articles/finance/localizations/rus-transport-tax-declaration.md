---
title: Декларация по транспортному налогу (Россия)
description: В данном разделе содержится информация о декларации по транспортному налогу для России.
author: anasyash
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-01-04
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d45feb3af1f1069e7f797001ccaea64c81dfc9ec
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000376"
---
# <a name="transport-tax-declaration-russia"></a><span data-ttu-id="c6114-103">Декларация по транспортному налогу (Россия)</span><span class="sxs-lookup"><span data-stu-id="c6114-103">Transport tax declaration (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6114-104">В соответствии с налоговым кодексом Российской Федерации автомобили облагаются транспортным налогом.</span><span class="sxs-lookup"><span data-stu-id="c6114-104">According to the tax code of the Russian Federation, vehicles are subject to transport tax.</span></span>

<span data-ttu-id="c6114-105">Налоговый период транспортного налога равен одному году.</span><span class="sxs-lookup"><span data-stu-id="c6114-105">The tax period for transport tax is one year.</span></span> <span data-ttu-id="c6114-106">В конце налогового периода компания должна подать декларацию по транспортному налогу.</span><span class="sxs-lookup"><span data-stu-id="c6114-106">At the end of the tax period, a company must report a transport tax declaration.</span></span>

<span data-ttu-id="c6114-107">Декларацию по транспортному налогу следует подавать в налоговый орган, где находится транспортное средство.</span><span class="sxs-lookup"><span data-stu-id="c6114-107">The transport tax declaration should be submitted to the tax authority where the vehicle is located.</span></span> <span data-ttu-id="c6114-108">В этом случае должен быть введен код **260** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="c6114-108">In this case, code **260** should be entered for the **at place of** attribute.</span></span> <span data-ttu-id="c6114-109">Однако крупнейшие налогоплательщики могут подавать декларации в налоговые органы по месту регистрации в качестве крупнейшего налогоплательщика.</span><span class="sxs-lookup"><span data-stu-id="c6114-109">However, the greatest taxpayers can submit declarations to the tax authority where the organization is registered as a greatest taxpayer.</span></span>
<span data-ttu-id="c6114-110">В этом случае должен быть введен код **216** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="c6114-110">In this case, code **216** should be entered for the **at place of** attribute.</span></span>

<span data-ttu-id="c6114-111">Налоговая база для расчета транспортного налога определяется по следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="c6114-111">The tax base for the calculation of transport tax is one of the following criteria:</span></span>

-   <span data-ttu-id="c6114-112">Мощность двигателя в лошадиных силах</span><span class="sxs-lookup"><span data-stu-id="c6114-112">Engine power, measured in horsepower</span></span>

-   <span data-ttu-id="c6114-113">Тяга двигателя, измеренная в килограммах силы</span><span class="sxs-lookup"><span data-stu-id="c6114-113">Jet thrust, measured in kilograms of the power</span></span>

-   <span data-ttu-id="c6114-114">Общая масса в тоннах, измеренная в объемных тоннах</span><span class="sxs-lookup"><span data-stu-id="c6114-114">Gross tonnage, measured in vessel tons</span></span>

<span data-ttu-id="c6114-115">Расчет транспортного налога включает все основные средства типа **Транспортное средство**, для которых запись основного средства содержит код транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-115">The transport tax calculation includes all fixed assets of the **Vehicle** asset type for which the fixed asset record contains a transport tax code.</span></span> <span data-ttu-id="c6114-116">Если основное средство списано или продано в течение учетного периода, расчет налога использует данные за месяц, когда произошли официальная регистрация и удаление из регистра.</span><span class="sxs-lookup"><span data-stu-id="c6114-116">If the fixed asset is written off or sold during the accounting period, the tax calculation uses data for the month when legal registration and removal from the register occurred.</span></span>

<span data-ttu-id="c6114-117">В этом раздел рассматривается, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="c6114-117">This topic explains how to perform the following tasks:</span></span>

1.  [<span data-ttu-id="c6114-118">Настройка транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-118">Set up transport tax</span></span>](#set-up-transport-tax)

2.  [<span data-ttu-id="c6114-119">Создание транспортного средства и настройка параметров для расчета транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-119">Create a vehicle and set up parameters for transport tax calculation</span></span>](#create-a-vehicle-and-set-up-parameters-for-transport-tax-calculation)

3.  [<span data-ttu-id="c6114-120">Расчет регистров транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-120">Calculate transport tax registers</span></span>](#calculate-transport-tax-registers)

4.  [<span data-ttu-id="c6114-121">Создание налоговой декларации по налогу на транспортировку</span><span class="sxs-lookup"><span data-stu-id="c6114-121">Generate a transport tax declaration</span></span>](#generate-a-transport-tax-declaration)

5.  [<span data-ttu-id="c6114-122">Создание и разноска проводок ГК по транспортному налогу</span><span class="sxs-lookup"><span data-stu-id="c6114-122">Create and post transport tax ledger transactions</span></span>](#create-and-post-transport-tax-ledger-transactions)

<a name="set-up-transport-tax"></a><span data-ttu-id="c6114-123">Настройка транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-123">Set up transport tax</span></span>
--------------------

<span data-ttu-id="c6114-124">Ниже приведен обзор шагов по настройке транспортного налога:</span><span class="sxs-lookup"><span data-stu-id="c6114-124">Here is an overview of the steps for setting up transport tax:</span></span>

1.  [<span data-ttu-id="c6114-125">Настройка кодов и ставок транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-125">Set up transport tax codes and rates</span></span>](#set-up-transport-tax-codes-and-rates)

2.  [<span data-ttu-id="c6114-126">Настройка кодов бюджетного дохода для транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-126">Set up budget revenue codes for transport tax</span></span>](#set-up-budget-revenue-codes-for-transport-tax)

3.  [<span data-ttu-id="c6114-127">Назначение кода бюджетного дохода налоговому коду</span><span class="sxs-lookup"><span data-stu-id="c6114-127">Assign a budget revenue code to a sales tax code</span></span>](#assign-a-budget-revenue-code-to-a-sales-tax-code)

4.  [<span data-ttu-id="c6114-128">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="c6114-128">Set up tax allowances</span></span>](#set-up-tax-allowances)

5.  [<span data-ttu-id="c6114-129">Назначение налоговых льгот налоговому коду как уменьшение ставки налога и уменьшение суммы налога</span><span class="sxs-lookup"><span data-stu-id="c6114-129">Assign tax allowances to a sales tax code as a reduction of the tax rate -and-a-reduction-of-the-tax-amount</span></span>](#assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-and-a-reduction-of-the tax amount)

6.  [<span data-ttu-id="c6114-130">Настройка групп и значений повышающих коэффициентов транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-130">Set up transport tax increasing factor groups and values</span></span>](#set-up-transport-tax-increasing-factor-groups-and-values)

7.  [<span data-ttu-id="c6114-131">Настройка кода территории (кода OKTMO) для юридического лица</span><span class="sxs-lookup"><span data-stu-id="c6114-131">Set up the territory code (OKTMO code) for the legal entity</span></span>](#set-up-the-territory-code-oktmo-code-for-the-legal-entity)

8.  [<span data-ttu-id="c6114-132">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="c6114-132">Set up tax authorities and related OKTMO codes</span></span>](#set-up-tax-authorities-and-related-oktmo-codes)

9.  [<span data-ttu-id="c6114-133">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="c6114-133">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>](#optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes)

10. [<span data-ttu-id="c6114-134">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="c6114-134">Set up the organization's locations and assign them to company divisions</span></span>](#set-up-the-organizations-locations-and-assign-them-to-company-divisions)

11. [<span data-ttu-id="c6114-135">Настройка параметров ОС для разноски транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-135">Set up Fixed assets parameters for posting transport tax</span></span>](#set-up-fixed-assets-parameters-for-posting-transport-tax)

12. [<span data-ttu-id="c6114-136">Настройка журнала для разноски транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-136">Set up the journal for posting transport tax</span></span>](#set-up-the-journal-for-posting-transport-tax)

13. [<span data-ttu-id="c6114-137">Настройка групп разноски для разносок транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-137">Set up a posting group for transport tax postings</span></span>](#set-up-a-posting-group-for-transport-tax-postings)

### <a name="set-up-transport-tax-codes-and-rates"></a><span data-ttu-id="c6114-138">Настройка кодов и ставок транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-138">Set up transport tax codes and rates</span></span>

1.  <span data-ttu-id="c6114-139">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="c6114-139">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>

2.  <span data-ttu-id="c6114-140">Создайте налоговый код.</span><span class="sxs-lookup"><span data-stu-id="c6114-140">Create a sales tax code.</span></span>

3.  <span data-ttu-id="c6114-141">В поле **Тип налога** выберите **Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-141">In the **Type of tax** field, select **Transport tax**.</span></span>

4.  <span data-ttu-id="c6114-142">Укажите период сопоставления и группу разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="c6114-142">Specify the settlement period and the ledger posting group.</span></span>

5.  <span data-ttu-id="c6114-143">В области действий на вкладке **Налоговый код** в группе **Налоговый код** выберите **Значения**, чтобы открыть страницу **Значения налогового кода**.</span><span class="sxs-lookup"><span data-stu-id="c6114-143">On the Action Pane, on the **Sales tax code** tab, in the **Sales tax code** group, select **Values** to open the **Sales tax code values** page.</span></span>

6.  <span data-ttu-id="c6114-144">Ставка транспортного налога зависит от типа и мощности транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-144">The transport tax rate depends on the type and power of the vehicle.</span></span> <span data-ttu-id="c6114-145">В полях **Нижний предел** и **Верхний предел** введите нижний и верхний пределы для интервала мощности.</span><span class="sxs-lookup"><span data-stu-id="c6114-145">In the **Lower Limit** and **Upper Limit** fields, enter lower and upper limits for the power interval.</span></span> <span data-ttu-id="c6114-146">Затем в поле **Значение** укажите ставку налога для указанного интервала.</span><span class="sxs-lookup"><span data-stu-id="c6114-146">Then, in the **Value** field, specify the tax rate for the specified interval.</span></span>

7.  <span data-ttu-id="c6114-147">В некоторых случаях ставка транспортного налога зависит также от фактического срока службы ТС.</span><span class="sxs-lookup"><span data-stu-id="c6114-147">In some cases, the transport tax rate also depends on the actual useful life of the vehicle.</span></span> <span data-ttu-id="c6114-148">Чтобы определить ставку налога так, чтобы она основывалась на сроке службы ТС, на панели операций на вкладке **Транспортный налог** в группе **Транспортный налог** выберите **По сроку службы**</span><span class="sxs-lookup"><span data-stu-id="c6114-148">To define the tax rate so that it's based on the vehicle's lifetime, on the Action Pane, on the **Transport tax** tab, in the **Transport tax** group, select **By lifetime**.</span></span> <span data-ttu-id="c6114-149">В полях **Нижний предел** и **Верхний предел** введите нижний и верхний пределы для срока службы.</span><span class="sxs-lookup"><span data-stu-id="c6114-149">In the **Minimum limit** and **Maximum limit** fields, enter the lower and upper limits for the lifetime.</span></span> <span data-ttu-id="c6114-150">Затем в поле **Ставка налога** укажите ставку налога для указанного интервала.</span><span class="sxs-lookup"><span data-stu-id="c6114-150">Then, in the **Tax value** field, specify the tax rate for the specified interval.</span></span>

### <a name="set-up-budget-revenue-codes-for-transport-tax"></a><span data-ttu-id="c6114-151">Настройка кодов бюджетного дохода для транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-151">Set up budget revenue codes for transport tax</span></span>

1.  <span data-ttu-id="c6114-152">Выберите **Управление банком и кассовыми операциями \> Настройка \> Настройка платежного поручения \> Классификация доходов бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="c6114-152">Go to **Cash and bank management \> Setup \> Payment order setup \> Budget revenue classification**.</span></span>

2.  <span data-ttu-id="c6114-153">Создайте код доходов бюджета для транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-153">Create a budget revenue code for transport tax.</span></span>

### <a name="assign-a-budget-revenue-code-to-a-sales-tax-code"></a><span data-ttu-id="c6114-154">Назначение кода бюджетного дохода налоговому коду</span><span class="sxs-lookup"><span data-stu-id="c6114-154">Assign a budget revenue code to a sales tax code</span></span>

1.  <span data-ttu-id="c6114-155">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="c6114-155">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="c6114-156">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="c6114-156">Create a record.</span></span>

3.  <span data-ttu-id="c6114-157">В поле **Тип налога** выберите **Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-157">In the **Type of tax** field, select **Transport tax**.</span></span>

4.  <span data-ttu-id="c6114-158">В поле **Код** выберите налоговый код транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-158">In the **Code** field, select the sales tax code for the transport tax.</span></span>

5.  <span data-ttu-id="c6114-159">В поле **Код доходов бюджета** выберите Код доходов бюджета, который соответствует выбранному налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="c6114-159">In the **Budget revenue code** field, select the budget revenue code that corresponds to the selected sales tax code.</span></span>

### <a name="set-up-tax-allowances"></a><span data-ttu-id="c6114-160">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="c6114-160">Set up tax allowances</span></span>

1.  <span data-ttu-id="c6114-161">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Налоговые льготы**.</span><span class="sxs-lookup"><span data-stu-id="c6114-161">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Tax allowances**.</span></span>

2.  <span data-ttu-id="c6114-162">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="c6114-162">Create a record.</span></span>

3.  <span data-ttu-id="c6114-163">Задайте следующие значения для налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="c6114-163">Set the following values for the tax allowance.</span></span>

| <span data-ttu-id="c6114-164">**Поле**</span><span class="sxs-lookup"><span data-stu-id="c6114-164">**Field**</span></span>                                          | <span data-ttu-id="c6114-165">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6114-165">**Description**</span></span>                                                                                                                                                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6114-166">**Привилегия**</span><span class="sxs-lookup"><span data-stu-id="c6114-166">**Privilege**</span></span>                                      | <span data-ttu-id="c6114-167">Введите коды налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="c6114-167">Enter the tax allowance code.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="c6114-168">**Тип налога**</span><span class="sxs-lookup"><span data-stu-id="c6114-168">**Type of tax**</span></span>                                    | <span data-ttu-id="c6114-169">Выберите **Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-169">Select **Transport tax**.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c6114-170">**Тип льготы**</span><span class="sxs-lookup"><span data-stu-id="c6114-170">**Benefit type**</span></span>                                   | <span data-ttu-id="c6114-171">Выберите тип налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="c6114-171">Select the type of tax allowance.</span></span> <span data-ttu-id="c6114-172">Следующие значения применяются для налоговых льгот по транспортному налогу: **Освобождение от налога**, **Снижение налоговой ставки**, **Уменьшение суммы налога** и **Налоговый вычет**.</span><span class="sxs-lookup"><span data-stu-id="c6114-172">The following values are applicable to transport tax allowances: **Exemption from tax**, **Reduction of tax rate**, **Reduction of tax amount**, and **Tax deduction**.</span></span> |
| <span data-ttu-id="c6114-173">**Название**</span><span class="sxs-lookup"><span data-stu-id="c6114-173">**Name**</span></span>                                           | <span data-ttu-id="c6114-174">Введите название налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="c6114-174">Enter the name of the tax allowance.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c6114-175">**Величина льготы**</span><span class="sxs-lookup"><span data-stu-id="c6114-175">**Allowance value**</span></span>                                | <span data-ttu-id="c6114-176">Определите значение налоговой льготы в зависимости от типа налоговой льготы, выбранного в поле **Тип льготы**:</span><span class="sxs-lookup"><span data-stu-id="c6114-176">Define the tax allowance value, depending on type of tax allowance that you selected in the **Benefit type** field:</span></span>                                                                                       |
| <span data-ttu-id="c6114-177">**Номер статьи**, **Пункт** и **Подпункт**</span><span class="sxs-lookup"><span data-stu-id="c6114-177">**Article number**, **Clause**, and **Sub-clause**</span></span> | <span data-ttu-id="c6114-178">Определите номер статьи, пункт и подпункт закона, в соответствии с которым предоставляется соответствующая налоговая скидка.</span><span class="sxs-lookup"><span data-stu-id="c6114-178">Define the article number, clause, and sub-clause of the law in accordance with which the corresponding tax allowance is granted.</span></span>                                                                         |

-   <span data-ttu-id="c6114-179">**Освобождение от налога:** не определяйте величину льготы, поскольку освобождение от налога всегда берется 100 процентов, а сумма налога составляет 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="c6114-179">**Exemption from tax:** Don't define the allowance value, because exemption from tax is always considered 100 percent, and the tax amount is 0 (zero).</span></span>

-   <span data-ttu-id="c6114-180">**Снижение налоговой ставки:** задайте процент уменьшения налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="c6114-180">**Reduction of tax rate:** Define the percentage of the tax rate reduction.</span></span>
    <span data-ttu-id="c6114-181">Например, если налоговая ставка равна 10 процентам, а налоговая льгота равна 2 процентам, уменьшенная налоговая ставка равна 8 процентам.</span><span class="sxs-lookup"><span data-stu-id="c6114-181">For example, if the tax rate is 10 percent, and the allowance value is 2 percent, the reduced tax rate is 8 percent.</span></span>

-   <span data-ttu-id="c6114-182">**Уменьшение суммы налога:** определите сумму, в местной валюте, на которую уменьшается рассчитанная сумма налога для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-182">**Reduction of tax amount:** Define the amount, in the local currency, that is reducing the calculated tax amount for each asset.</span></span>

### <a name="assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-and-a-reduction-of-the-tax-amount"></a><span data-ttu-id="c6114-183">Назначение налоговых льгот налоговому коду как уменьшение ставки налога и уменьшение суммы налога</span><span class="sxs-lookup"><span data-stu-id="c6114-183">Assign tax allowances to a sales tax code as a reduction of the tax rate and a reduction of the tax amount</span></span>

1.  <span data-ttu-id="c6114-184">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="c6114-184">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="c6114-185">Выберите запись для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="c6114-185">Select the record for the sales tax code.</span></span>

3.  <span data-ttu-id="c6114-186">В полях **Льгота путем понижения ставки** и **Льгота путем уменьшения налога** выберите соответствующие налоговые льготы, если они применимы к налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="c6114-186">In the **Allowance by reduction of rate** and **Allowance by reduction of tax** fields, select the appropriate tax allowances, if they are applicable to the sales tax code.</span></span>

### <a name="set-up-transport-tax-increasing-factor-groups-and-values"></a><span data-ttu-id="c6114-187">Настройка групп и значений повышающих коэффициентов транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-187">Set up transport tax increasing factor groups and values</span></span>

<span data-ttu-id="c6114-188">Сумма транспортного налога должна быть увеличена для дорогостоящих моделей транспортных средств, перечень которых определяется Министерством промышленности и торговли в информационном письме и ежегодно пересматривается.</span><span class="sxs-lookup"><span data-stu-id="c6114-188">The amount of transport tax should be increased for expensive vehicle models that are defined by the Ministry of Production and Trade in an informational letter and annually reviewed.</span></span> <span data-ttu-id="c6114-189">Коэффициент, который должен учитываться, зависит от числа лет, которые прошли с момента изготовления автомобиля, и стоимости ТС.</span><span class="sxs-lookup"><span data-stu-id="c6114-189">The coefficient that must be considered depends on both the number of years that have passed since the vehicle's year of manufacture and the cost of vehicle.</span></span> <span data-ttu-id="c6114-190">Например, для ТС стоимостью от 3 до 5 млн рублей, если с года производства прошло менее одного года, коэффициент увеличения составляет 1,5.</span><span class="sxs-lookup"><span data-stu-id="c6114-190">For example, for a vehicle that costs between 3 million and 5 million rubles, if less than one year has passed since its year of manufacture, the increasing coefficient is 1.5.</span></span>

1.  <span data-ttu-id="c6114-191">Перейдите в раздел **Основное средство (Россия) \> Настройка \> Налоговая отчетность \> Группы повышающих коэффициентов транспортного налога**.</span><span class="sxs-lookup"><span data-stu-id="c6114-191">Go to **Fixed asset (Russia) \> Setup \> Tax reporting \> Transport tax increasing factor groups**.</span></span>

2.  <span data-ttu-id="c6114-192">Создайте группу.</span><span class="sxs-lookup"><span data-stu-id="c6114-192">Create a group.</span></span>

3.  <span data-ttu-id="c6114-193">На экспресс -вкладке **Значения повышающего коэффициента транспортного налога** определите следующие значения повышающего коэффициента.</span><span class="sxs-lookup"><span data-stu-id="c6114-193">On the **Transport tax increasing factor values** FastTab, define the following increasing factor values.</span></span>

| <span data-ttu-id="c6114-194">**Поле**</span><span class="sxs-lookup"><span data-stu-id="c6114-194">**Field**</span></span>      | <span data-ttu-id="c6114-195">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6114-195">**Description**</span></span>                                                                          |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6114-196">с даты</span><span class="sxs-lookup"><span data-stu-id="c6114-196">From date</span></span>      | <span data-ttu-id="c6114-197">Введите дату, с которой начинается применение значения коэффициента.</span><span class="sxs-lookup"><span data-stu-id="c6114-197">Enter the date when the factor value starts to apply.</span></span>                                    |
| <span data-ttu-id="c6114-198">Верхний предел срока службы</span><span class="sxs-lookup"><span data-stu-id="c6114-198">Upper lifetime</span></span> | <span data-ttu-id="c6114-199">Введите верхний предел срока службы в даты выпуска, к которому применяется коэффициент.</span><span class="sxs-lookup"><span data-stu-id="c6114-199">Enter the upper limit of the lifetime from manufacture that the factor value applies to.</span></span> |
| <span data-ttu-id="c6114-200">Множитель</span><span class="sxs-lookup"><span data-stu-id="c6114-200">Factor</span></span>         | <span data-ttu-id="c6114-201">Введите повышающий коэффициент.</span><span class="sxs-lookup"><span data-stu-id="c6114-201">Enter the increasing factor.</span></span>                                                             |

### <a name="set-up-the-territory-code-oktmo-code-for-the-legal-entity"></a><span data-ttu-id="c6114-202">Настройка кода территории (кода OKTMO) для юридического лица</span><span class="sxs-lookup"><span data-stu-id="c6114-202">Set up the territory code (OKTMO code) for the legal entity</span></span>

1.  <span data-ttu-id="c6114-203">Перейдите в раздел **Управление организацией \> Организации \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="c6114-203">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

2.  <span data-ttu-id="c6114-204">На экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="c6114-204">On the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

3.  <span data-ttu-id="c6114-205">На странице **Управление адресами** на экспресс-вкладке **Регистрационный номер** создайте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-205">On the **Manage addresses** page, on the **Registration ID** FastTab, create a line.</span></span>

4.  <span data-ttu-id="c6114-206">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="c6114-206">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

>   <span data-ttu-id="c6114-207">Если требуемый тип регистрации отсутствует в списке, выполните следующие действия, чтобы добавить его:</span><span class="sxs-lookup"><span data-stu-id="c6114-207">If the required registration type isn't listed, follow these steps to add   it:</span></span>

1.  <span data-ttu-id="c6114-208">На странице **Типы регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Типы регистрации**) создайте тип регистрации.</span><span class="sxs-lookup"><span data-stu-id="c6114-208">On the **Registration types** page (**Organization administration \> Global address book \> Registration types \> Registration types**), create a registration type.</span></span>

2.  <span data-ttu-id="c6114-209">На странице **Категории регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Категории регистрации**) назначьте новый тип регистрации категории регистрации **ОКАТО**.</span><span class="sxs-lookup"><span data-stu-id="c6114-209">On the **Registration categories** page (**Organization administration \> Global address book \> Registration types \> Registration categories**), assign the new registration type to the **RCOAD** registration category.</span></span>

3.  <span data-ttu-id="c6114-210">В поле **Регистрационный номер** введите код OKTMO для местоположения юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c6114-210">In the **Registration number** field, enter the OKTMO code for the legal entity's location.</span></span>

### <a name="set-up-tax-authorities-and-related-oktmo-codes"></a><span data-ttu-id="c6114-211">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="c6114-211">Set up tax authorities and related OKTMO codes</span></span>

<span data-ttu-id="c6114-212">Необходимо создать налоговые органы, в который вы должны подавать декларации по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="c6114-212">You must create the tax authorities that you're required to report assessed tax declarations to.</span></span>

1.  <span data-ttu-id="c6114-213">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="c6114-213">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax authorities**.</span></span>

2.  <span data-ttu-id="c6114-214">Создайте налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="c6114-214">Create a tax authority.</span></span>

3.  <span data-ttu-id="c6114-215">Задайте поля **Налоговый орган** и **Название**.</span><span class="sxs-lookup"><span data-stu-id="c6114-215">Set the **Authority** and **Name** fields.</span></span>

4.  <span data-ttu-id="c6114-216">В поле **Код ГНИ** введите четырехзначный код для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="c6114-216">In the **STI code** field, enter the four-digit code for the tax authority.</span></span>

5.  <span data-ttu-id="c6114-217">В поле **Счет поставщика** выберите субъект счета поставщика, который связан с налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="c6114-217">In the **Vendor account** field, select the vendor account party that is associated with the tax authority.</span></span>

6.  <span data-ttu-id="c6114-218">Определите основной код OKTMO для налогового органа для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="c6114-218">Define the main OKTMO code for the tax authority on the vendor account:</span></span>

    1.  <span data-ttu-id="c6114-219">В записи для счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="c6114-219">In the record for the vendor account, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="c6114-220">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-220">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="c6114-221">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="c6114-221">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="c6114-222">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="c6114-222">In the **Registration number** field, enter the OKTMO code.</span></span>

        <span data-ttu-id="c6114-223">**Примечание.** Для объектов недвижимости, которые расположены в главном расположении организации, налоговый орган, в который подается отчет по налогу на имущество, определяется как в налоговый орган, имеющий такой же код OKTMO, как и у юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c6114-223">**Note:** For realty objects that are located at the organization's main location, the tax authority that assessed tax is reported to is defined as the tax authority that has the same OKTMO code as the legal entity.</span></span>

### <a name="optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes"></a><span data-ttu-id="c6114-224">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="c6114-224">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>

<span data-ttu-id="c6114-225">Если у организации имеются объекты недвижимости, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить подразделения компании.</span><span class="sxs-lookup"><span data-stu-id="c6114-225">If the organization has realty objects that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up company divisions.</span></span>

1.  <span data-ttu-id="c6114-226">Выберите **Управления организацией \> Настройка \> Обособленные подразделения**.</span><span class="sxs-lookup"><span data-stu-id="c6114-226">Go to **Organization administration \> Setup \> Separate divisions**.</span></span>

2.  <span data-ttu-id="c6114-227">Создание отдела компании.</span><span class="sxs-lookup"><span data-stu-id="c6114-227">Create a company division.</span></span>

3.  <span data-ttu-id="c6114-228">В поле **Код отдельного подразделения** введите идентификационный код для подразделения.</span><span class="sxs-lookup"><span data-stu-id="c6114-228">In the **Separate division ID** field, enter the identification code for the division.</span></span>

4.  <span data-ttu-id="c6114-229">В поле **Имя** введите имя подразделения.</span><span class="sxs-lookup"><span data-stu-id="c6114-229">In the **Name** field, enter the name of the division.</span></span>

5.  <span data-ttu-id="c6114-230">В поле **Счет поставщика** выберите номер счета поставщика, который связан с отделом.</span><span class="sxs-lookup"><span data-stu-id="c6114-230">In the **Vendor account** field, select the vendor account number that is associated with the division.</span></span> <span data-ttu-id="c6114-231">Если ни один счет поставщика недоступен для подразделения компании, необходимо создать счет.</span><span class="sxs-lookup"><span data-stu-id="c6114-231">If there is no vendor account for the company division, create one.</span></span>

6.  <span data-ttu-id="c6114-232">Определите код OKTMO для подразделения компании для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="c6114-232">Define the OKTMO code for the company division on the vendor account:</span></span>

    1.  <span data-ttu-id="c6114-233">В записи счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="c6114-233">In the vendor account record, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="c6114-234">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-234">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="c6114-235">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="c6114-235">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="c6114-236">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="c6114-236">In the **Registration number** field, enter the OKTMO code.</span></span>

7.  <span data-ttu-id="c6114-237">Повторите шаг 6, чтобы определить код КПП для обособленного подразделения для счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="c6114-237">Repeat step 6 to define the KPP code for the separate division on the vendor account.</span></span> <span data-ttu-id="c6114-238">В поле **Тип регистрации** выберите тип регистрации, с которым связана категория регистрации **КПП**.</span><span class="sxs-lookup"><span data-stu-id="c6114-238">In the **Registration type** field, select the registration type that is associated with the **KPP** registration category.</span></span>

### <a name="set-up-the-organizations-locations-and-assign-them-to-company-divisions"></a><span data-ttu-id="c6114-239">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="c6114-239">Set up the organization's locations and assign them to company divisions</span></span>

<span data-ttu-id="c6114-240">Если у организации имеются объекты недвижимости, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить местоположения организации и назначить их подразделениям компании.</span><span class="sxs-lookup"><span data-stu-id="c6114-240">If the organization has realty objects that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up organization locations and assign them to company divisions.</span></span>

1.  <span data-ttu-id="c6114-241">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="c6114-241">Go to **Fixed assets (Russia) \> Setup \> Location**.</span></span>

2.  <span data-ttu-id="c6114-242">Выберите существующее местоположение или создайте новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="c6114-242">Select an existing location, or create a new location.</span></span>

3.  <span data-ttu-id="c6114-243">На экспресс-вкладке **Общие** в поле **Код отдельного подразделения** выберите подразделение компании, созданное в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="c6114-243">On the **General** FastTab, in the **Separate division ID** field, select the company division that you created in the previous procedure.</span></span>

    <span data-ttu-id="c6114-244">**Примечание.** Для транспортных средств, которые зарегистрированы на территориях, отличающихся от главного расположения организации, налоговый орган, в который подается отчет по транспортному налогу, определяется как в налоговый орган с тем же кодом OKTMO, что и у обособленного подразделения, связанного с местоположением транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-244">**Note:** For vehicles that are registered in territories that differ from the organization's main location, the tax authority that transport tax is reported to is defined as the tax authority that has the same OKTMO code as the separate division that is associated with the vehicle location.</span></span> <span data-ttu-id="c6114-245">Сведения о том, как связать основное средство с местоположением, см. в разделе [Указание местоположения транспортного средства](#specify-the-location-of-the-vehicle) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c6114-245">For information about how to associate a fixed asset with a location, see the [Specify the location of the vehicle](#specify-the-location-of-the-vehicle) section later in this topic.</span></span>

    <span data-ttu-id="c6114-246">Если поле **Код отдельного подразделения** оставлено пустым, местоположение совпадает с местоположением головного офиса организации.</span><span class="sxs-lookup"><span data-stu-id="c6114-246">If the **Separate division ID** field is left blank, the location is the same as the location of the organization's head office.</span></span>

### <a name="set-up-fixed-assets-parameters-for-posting-transport-tax"></a><span data-ttu-id="c6114-247">Настройка параметров ОС для разноски транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-247">Set up Fixed assets parameters for posting transport tax</span></span>

1.  <span data-ttu-id="c6114-248">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="c6114-248">Go to **Fixed assets (Russia) \> Setup \> Parameters**.</span></span>

2.  <span data-ttu-id="c6114-249">На вкладке **Номерные серии** для ссылки **Номер журнала регистров налога на имущество** выберите номерную серию для налогового регистра.</span><span class="sxs-lookup"><span data-stu-id="c6114-249">On the **Number sequences** tab, for the **Assessed tax registers journal number** reference, select a number sequence for the tax register.</span></span>

3.  <span data-ttu-id="c6114-250">На вкладке **Налоговая отчетность** в разделе **Транспортный налог** в поле **Код налога** выберите код налога по умолчанию для транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-250">On the **Tax reporting** tab, in the **Transport tax** section, in the **Sales tax code** field, select the default sales tax code for transport tax.</span></span>

4.  <span data-ttu-id="c6114-251">В поле **Сжатие** выберите уровень сжатия для проводок транспортного налога:</span><span class="sxs-lookup"><span data-stu-id="c6114-251">In the **Compression** field, select the level of compression for transport tax transactions:</span></span>

-   <span data-ttu-id="c6114-252">**Налог** — подробный журнал книги учета для проводок по транспортному налогу будет создаваться для каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="c6114-252">**Tax** – A detailed ledger journal for transport tax transactions will be created for each sales tax code.</span></span>

-   <span data-ttu-id="c6114-253">**Итог** — журнал книги учета для проводок транспортного налога будет создаваться как одна строка с кодом налога по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6114-253">**Total** – A ledger journal for transport tax transactions will be created as one line that has the default sales tax code.</span></span>

1.  <span data-ttu-id="c6114-254">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c6114-254">Close the page.</span></span>

### <a name="set-up-the-journal-for-posting-transport-tax"></a><span data-ttu-id="c6114-255">Настройка журнала для разноски транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-255">Set up the journal for posting transport tax</span></span>

<span data-ttu-id="c6114-256">Если проводки по транспортному налогу будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить журнал.</span><span class="sxs-lookup"><span data-stu-id="c6114-256">If transport tax transactions will be automatically created based on calculated tax registers, you should set up a journal.</span></span>

1.  <span data-ttu-id="c6114-257">Перейдите в раздел **Главная книга \> Настройка журнала \> Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="c6114-257">Go to **General ledger \> Journal setup \> Journal names**.</span></span>

2.  <span data-ttu-id="c6114-258">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-258">Create a line.</span></span>

3.  <span data-ttu-id="c6114-259">Задайте поля **Название** и **Серии ваучеров**.</span><span class="sxs-lookup"><span data-stu-id="c6114-259">Set the **Name** and **Voucher series** fields.</span></span>

4.  <span data-ttu-id="c6114-260">В поле **Тип журнала** выберите **Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-260">In the **Journal type** field, select **Transport tax**.</span></span>

### <a name="set-up-a-posting-group-for-transport-tax-postings"></a><span data-ttu-id="c6114-261">Настройка групп разноски для разносок транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-261">Set up a posting group for transport tax postings</span></span>

<span data-ttu-id="c6114-262">Если проводки по транспортному налогу будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить группы разноски.</span><span class="sxs-lookup"><span data-stu-id="c6114-262">If transport tax transactions will be automatically created based on calculated tax registers, you should set up posting groups.</span></span>

1.  <span data-ttu-id="c6114-263">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Группа разноски по налогам**.</span><span class="sxs-lookup"><span data-stu-id="c6114-263">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Group of posting of taxes**.</span></span>

2.  <span data-ttu-id="c6114-264">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-264">Create a line.</span></span>

3.  <span data-ttu-id="c6114-265">В поле **Группа разноски ГК** выберите группу разноски ГК для транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-265">In the **Ledger posting group** field, select a ledger posting group for transport tax.</span></span>

>   <span data-ttu-id="c6114-266">Если в списке нет ни одной группы разноски ГК, создайте ее.</span><span class="sxs-lookup"><span data-stu-id="c6114-266">If no ledger posting group is listed, create one.</span></span> <span data-ttu-id="c6114-267">В поле **Исходящий налог** введите номер счета ГК для разноски транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-267">In the **Sales tax payable** field, enter the ledger account code for posting transport tax.</span></span>

1.  <span data-ttu-id="c6114-268">В поле **Счет для налогов ОС** выберите счет ГК для расходов по транспортному налогу.</span><span class="sxs-lookup"><span data-stu-id="c6114-268">In the **Account for FA taxes** field, select a ledger account for the transport tax expenses.</span></span>

2.  <span data-ttu-id="c6114-269">Убедитесь, что в поле **Исходящий налог** установлено значение кода счета ГК, введенного для группы разноски главной книги на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="c6114-269">Make sure that the **Sales tax payable** field is set to the ledger account code that you entered for the ledger posting group in step 3.</span></span>

<a name="create-a-vehicle-and-set-up-parameters-for-transport-tax-calculation"></a><span data-ttu-id="c6114-270">Создание транспортного средства и настройка параметров для расчета транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-270">Create a vehicle and set up parameters for transport tax calculation</span></span>
--------------------------------------------------------------------

<span data-ttu-id="c6114-271">Ниже приведен обзор шагов для создания транспортного средства и настройки параметров для расчета транспортного налога:</span><span class="sxs-lookup"><span data-stu-id="c6114-271">Here is an overview of the steps for creating a vehicle and setting up parameters for transport tax calculation:</span></span>

1.  [<span data-ttu-id="c6114-272">Создание транспортного средства и определение параметров для расчета транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-272">Create a vehicle fixed asset and define parameters for transport tax calculation</span></span>](#create-a-vehicle-fixed-asset-and-define-parameters-for-transport-tax-calculation)

2.  [<span data-ttu-id="c6114-273">Указание местоположения транспортного средства</span><span class="sxs-lookup"><span data-stu-id="c6114-273">Specify the location of the vehicle</span></span>](#specify-the-location-of-the-vehicle)

3.  [<span data-ttu-id="c6114-274">Указание налоговой льготы как освобождение от налога</span><span class="sxs-lookup"><span data-stu-id="c6114-274">Specify a tax allowance as an exemption from tax</span></span>](#specify-a-tax-allowance-as-an-exemption-from-tax)

### <a name="create-a-vehicle-fixed-asset-and-define-parameters-for-transport-tax-calculation"></a><span data-ttu-id="c6114-275">Создание транспортного средства и определение параметров для расчета транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-275">Create a vehicle fixed asset and define parameters for transport tax calculation</span></span>

1.  <span data-ttu-id="c6114-276">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="c6114-276">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="c6114-277">Выберите существующее основное средство или создайте новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="c6114-277">Select an existing fixed asset, or create a new fixed asset.</span></span>

3.  <span data-ttu-id="c6114-278">На экспресс-вкладке **Общее** в поле **Тип** выберите **Транспортное средство**.</span><span class="sxs-lookup"><span data-stu-id="c6114-278">On the **General** FastTab, in the **Type** field, select **Vehicle**.</span></span>

4.  <span data-ttu-id="c6114-279">В поле **Флаг владения** выберите, находится ли основное средство в собственности, операционном управлении, аренде или владении лица за пределами России.</span><span class="sxs-lookup"><span data-stu-id="c6114-279">In the **Flag of ownership** field, select whether the fixed asset is owned, under operational management, leased, or owned by someone who is outside Russia.</span></span>

5.  <span data-ttu-id="c6114-280">На экспресс-вкладке **Техническая информация** в разделе **Транспортное средство** задайте поля **Вид ТС**, **Модель**, **Регистрационный номер** и **Класс эмиссии**.</span><span class="sxs-lookup"><span data-stu-id="c6114-280">On the **Technical information** FastTab, in the **Vehicle** section, set the **Vehicle type**, **Model**, **Registration number**, and **Emission class** fields.</span></span>

>   <span data-ttu-id="c6114-281">**Примечание.** Типы транспортных средств создаются на странице **Виды транспортных средств** (**Основные средства (Россия) \> Настройка \> Транспортное средство \> Виды ТС**).</span><span class="sxs-lookup"><span data-stu-id="c6114-281">**Note:** You create vehicle types on the **Vehicle types** page (**Fixed assets (Russia) \> Setup \> Vehicle \> Vehicle types**).</span></span> <span data-ttu-id="c6114-282">Модели транспортных средств создаются на странице **Модели транспортных средств** (**Основные средства (Россия) \> Настройка \> Транспортное средство \> Модели транспортных средств**).</span><span class="sxs-lookup"><span data-stu-id="c6114-282">You create vehicle models on the **Vehicle models** page (**Fixed assets (Russia) \> Setup \> Vehicle \> Vehicle models**).</span></span>

1.  <span data-ttu-id="c6114-283">В разделе **Срок полезного использования** в поле **Год выпуска** укажите год изготовления.</span><span class="sxs-lookup"><span data-stu-id="c6114-283">In the **Useful life** section, in the **Output year** field, specify the year of manufacture.</span></span>

2.  <span data-ttu-id="c6114-284">В разделе **Государственная регистрация** задайте поля **Дата регистрации** и **Дата удаления из регистра**.</span><span class="sxs-lookup"><span data-stu-id="c6114-284">In the **Government registration** section, set the **Date of the registration** and **Removal from the register date** fields.</span></span>

3.  <span data-ttu-id="c6114-285">На экспресс-вкладке **Налоговая отчетность** в разделе **Транспортный налог** в поле **Налоговая база** введите мощность ТС.</span><span class="sxs-lookup"><span data-stu-id="c6114-285">On the **Tax reporting** FastTab, in the **Transport tax** section, in the field **Tax base** field, specify the vehicle power.</span></span> <span data-ttu-id="c6114-286">В поле **Единица** укажите единицу измерения мощности транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-286">In the **Unit** field, specify the unit of measure for the vehicle power.</span></span>

4.  <span data-ttu-id="c6114-287">Если вы частично владеете основным средством, в полях **Числитель доли собственности** и **Знаменатель доли собственности** определите свою долю собственности в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="c6114-287">If you partially own the fixed asset, in the **Owned share numerator** and **Owned share denominator** fields, define your ownership share as a simple fraction.</span></span>

5.  <span data-ttu-id="c6114-288">В поле **Налоговый код** выберите налоговый код для расчета налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="c6114-288">In the **Sales tax code** field, select the sales tax code for the assessed tax calculation.</span></span>

6.  <span data-ttu-id="c6114-289">Задайте поле **Группа повышающих коэффициентов**.</span><span class="sxs-lookup"><span data-stu-id="c6114-289">Set the **Increasing factor group** field.</span></span>

7.  <span data-ttu-id="c6114-290">В поле **Вычет** укажите код налогового вычета.</span><span class="sxs-lookup"><span data-stu-id="c6114-290">In the **Deduction** field, specify the tax deduction code.</span></span> <span data-ttu-id="c6114-291">В поле **Сумма налогового вычета** укажите сумму налогового вычета.</span><span class="sxs-lookup"><span data-stu-id="c6114-291">In the **Tax deduction amount** field, specify the deduction amount.</span></span>

### <a name="specify-the-location-of-the-vehicle"></a><span data-ttu-id="c6114-292">Указание местоположения транспортного средства</span><span class="sxs-lookup"><span data-stu-id="c6114-292">Specify the location of the vehicle</span></span>

<span data-ttu-id="c6114-293">По умолчанию предполагается, что транспортные средства расположены в месте расположения организации и отчет о них направляется налоговым органам на территории юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c6114-293">By default, the assumption is that vehicles are located at the organization's location and reported to the tax authority in the legal entity's territory.</span></span> <span data-ttu-id="c6114-294">(Код налогового органа OKTMO соответствует коду OKTMO юридического лица, и объекты недвижимости включаются в отчет под тем же кодом OKTMO.)</span><span class="sxs-lookup"><span data-stu-id="c6114-294">(The OKTMO code of the tax authority matches the OKTMO code of the legal entity, and realty objects are reported under the same OKTMO code.)</span></span>

<span data-ttu-id="c6114-295">Если у организации есть транспортные средства, которые находятся на других территориях и зарегистрированы в других налоговых органах, необходимо указать местоположение транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-295">If the organization has vehicles that are located in different territories and registered in different tax authorities, you must specify the location of the vehicle.</span></span>

1.  <span data-ttu-id="c6114-296">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="c6114-296">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="c6114-297">Выберите строку для транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-297">Select the line for the vehicle.</span></span>

3.  <span data-ttu-id="c6114-298">В области действий на вкладке **Основные средства** в группе **История** выберите **Передача**.</span><span class="sxs-lookup"><span data-stu-id="c6114-298">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Transfer**.</span></span>

4.  <span data-ttu-id="c6114-299">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-299">Create a line.</span></span>

5.  <span data-ttu-id="c6114-300">Задайте поля **Дата** и **Новое местоположение**.</span><span class="sxs-lookup"><span data-stu-id="c6114-300">Set the **Date** and **New location** fields.</span></span>

### <a name="specify-a-tax-allowance-as-an-exemption-from-tax"></a><span data-ttu-id="c6114-301">Указание налоговой льготы как освобождение от налога</span><span class="sxs-lookup"><span data-stu-id="c6114-301">Specify a tax allowance as an exemption from tax</span></span> 

1.  <span data-ttu-id="c6114-302">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="c6114-302">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="c6114-303">Выберите строку для транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-303">Select the line for the vehicle.</span></span>

3.  <span data-ttu-id="c6114-304">В области действий на вкладке **Основные средства** в группе **История** выберите **Данные налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="c6114-304">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Tax reporting data**.</span></span>

4.  <span data-ttu-id="c6114-305">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="c6114-305">Create a line.</span></span>

5.  <span data-ttu-id="c6114-306">В поле **Период** укажите месяц, когда действует налоговая льгота как освобождение от налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-306">In the **Period** field, specify the month when a tax allowance as an exemption from tax applies.</span></span> <span data-ttu-id="c6114-307">В поле **Освобождение от налога** выберите код налоговой льготы в виде освобождения от налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-307">In the **Exemption from tax** field, select the code for the tax allowance as an exemption from tax.</span></span>

<a name="calculate-transport-tax-registers"></a><span data-ttu-id="c6114-308">Расчет регистров транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-308">Calculate transport tax registers</span></span>
---------------------------------

<span data-ttu-id="c6114-309">После завершения настройки, регистрации приобретения транспортного средства и настройки всех параметров транспортных средств для расчета транспортного налога, необходимо рассчитать регистры транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-309">After you've finished the setup, registered the acquisition of the vehicle, and set up all vehicle parameters for transport tax calculation, you must calculate transport tax registers.</span></span> <span data-ttu-id="c6114-310">Доступны следующие налоговые регистры:</span><span class="sxs-lookup"><span data-stu-id="c6114-310">The following tax registers are available:</span></span>

-   <span data-ttu-id="c6114-311">**Транспортное средство — расчет налога** — этот налоговый регистр рассчитывает транспортный налог для каждого транспортного средства.</span><span class="sxs-lookup"><span data-stu-id="c6114-311">**Vehicle - tax calculation** – This tax register calculates transport tax for each vehicle.</span></span> <span data-ttu-id="c6114-312">В нем отображается следующая информация:</span><span class="sxs-lookup"><span data-stu-id="c6114-312">It shows the following information:</span></span>

    -   <span data-ttu-id="c6114-313">Тип ТС, серийный номер, модель и регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="c6114-313">The vehicle type, serial number, model, and registration number.</span></span>

    -   <span data-ttu-id="c6114-314">Даты регистрации и удаления транспортных средств из регистра.</span><span class="sxs-lookup"><span data-stu-id="c6114-314">The dates of vehicle registration and removal from the register.</span></span>

    -   <span data-ttu-id="c6114-315">Налоговая база и единицы измерения для налоговой базы.</span><span class="sxs-lookup"><span data-stu-id="c6114-315">The tax base and the units of measure for the tax base.</span></span>

    -   <span data-ttu-id="c6114-316">Полезный срок службы, в годах, после года изготовления и года выпуска.</span><span class="sxs-lookup"><span data-stu-id="c6114-316">The useful lifetime, in years, after the year of manufacture, and the output year.</span></span>

    -   <span data-ttu-id="c6114-317">Доля собственности в качестве свидетельства частичного владения транспортным средством.</span><span class="sxs-lookup"><span data-stu-id="c6114-317">The owned share as an indication that the vehicle is partially owned.</span></span>

    -   <span data-ttu-id="c6114-318">**Коэффициент Кп** — повышающий коэффициент для дорогостоящих транспортных средств.</span><span class="sxs-lookup"><span data-stu-id="c6114-318">**Factor Kp** – The increasing factor for expensive vehicles.</span></span>

    -   <span data-ttu-id="c6114-319">Коэффициент владения, если транспортное средство было приобретено или продано в течение периода.</span><span class="sxs-lookup"><span data-stu-id="c6114-319">The ownership factor if the vehicle was acquired or sold during the period.</span></span> <span data-ttu-id="c6114-320">Этот коэффициент представляет собой отношение периода владения к количеству календарных месяцев в периоде.</span><span class="sxs-lookup"><span data-stu-id="c6114-320">This factor is the ratio of the ownership period to the number of calendar months in the period.</span></span>

    -   <span data-ttu-id="c6114-321">**Рассчитанный авансовый платеж/налог** — если налоговый регистр рассчитывается для первого квартала, второго квартала или третьего квартала, сумма налогового аванса до применения налоговых вычетов.</span><span class="sxs-lookup"><span data-stu-id="c6114-321">**Calculated advance payment / Tax** – If the tax register is calculated for the first quarter, second quarter, or third quarter, the tax advance amount before tax allowances are applied.</span></span> <span data-ttu-id="c6114-322">Если налоговый регистр рассчитывается за год, применяется сумма транспортного налога до применения налоговых вычетов.</span><span class="sxs-lookup"><span data-stu-id="c6114-322">If the tax register is calculated for the year, the transport tax amount before tax allowances are applied.</span></span>

    -   <span data-ttu-id="c6114-323">**Освобождение от налога** — код налоговой льготы в виде освобождения от налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-323">**Exemption from tax** – The code for the tax allowance as an exemption from tax.</span></span>

    -   <span data-ttu-id="c6114-324">Сумма налоговой льготы как освобождение от налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-324">The amount of the tax allowance as an exemption from tax.</span></span>

    -   <span data-ttu-id="c6114-325">**Льготный период** — количество месяцев, в течение которых нет исключения налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="c6114-325">**Grace period** – The number of months when there is no tax exemption allowance.</span></span>

    -   <span data-ttu-id="c6114-326">**Льготный коэффициент** — отношение льготного периода к количеству календарных месяцев в налоговом периоде.</span><span class="sxs-lookup"><span data-stu-id="c6114-326">**Allowance factor** – The ratio of the grace period to the number of calendar months in the tax period.</span></span>

    -   <span data-ttu-id="c6114-327">**Код льготы** — код налоговой льготы в виде уменьшения ставки или сокращения налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-327">**Privilege** – The code for the tax allowance as a reduction of the rate or a reduction of tax.</span></span>

    -   <span data-ttu-id="c6114-328">**Сумма налоговой льготы** — сумма налоговой льготы в виде уменьшения налоговой ставки или уменьшения суммы налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-328">**Tax allowance amount** – The amount of the tax allowance as a reduction of the tax rate or a reduction of the tax amount.</span></span>

    -   <span data-ttu-id="c6114-329">**Вычет** — код налогового вычета.</span><span class="sxs-lookup"><span data-stu-id="c6114-329">**Deduction** – The code for the tax deduction.</span></span>

    -   <span data-ttu-id="c6114-330">**Сумма налоговой льготы** — сумма налогового вычета.</span><span class="sxs-lookup"><span data-stu-id="c6114-330">**Tax allowance amount** – The amount of the tax deduction.</span></span>

    -   <span data-ttu-id="c6114-331">Ставка транспортного налога, код доходов бюджета, код отдельного подразделения и местоположение ТС, а также налоговый орган, которому сообщается о транспортном налоге.</span><span class="sxs-lookup"><span data-stu-id="c6114-331">The transport tax rate, budget revenue code, separate division ID, and location of the vehicle, and the tax authority that the tax for the vehicle will be reported to.</span></span>

-   <span data-ttu-id="c6114-332">**Транспортный налог** — этот налоговый регистр рассчитывает итоговые суммы транспортного налога для каждого налогового кода и кода OKTMO.</span><span class="sxs-lookup"><span data-stu-id="c6114-332">**Transport tax** – This tax register calculates total transport tax amounts for each sales tax code and OKTMO code.</span></span>

>   <span data-ttu-id="c6114-333">Чтобы рассчитать и утвердить регистры транспортного налога, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6114-333">To calculate and approve transport tax registers, follow these steps.</span></span>

1.  <span data-ttu-id="c6114-334">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="c6114-334">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="c6114-335">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c6114-335">Select **New**.</span></span>

3.  <span data-ttu-id="c6114-336">В поле **Тип налога** выберите **Транспортный налог** для создания журнала только для регистров транспортного налога или оставьте это поле пустым, чтобы создать журнал для всех налогов на ОС (налога на имущество, земельного налога и транспортного налога).</span><span class="sxs-lookup"><span data-stu-id="c6114-336">In the **Type of tax** field, either select **Transport tax** to create a journal only for transport tax registers, or leave the field blank to create a journal for all the asset's taxes (assessed tax, land tax, and transport tax).</span></span>

4.  <span data-ttu-id="c6114-337">В поле **Типы периодов** выберите один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c6114-337">In the **Period types** field, select one of the following values:</span></span>

    -   <span data-ttu-id="c6114-338">**Квартал** — создание журнала для расчета авансовых платежей по транспортному налогу.</span><span class="sxs-lookup"><span data-stu-id="c6114-338">**Quarter** – Generate a journal for the calculation of transport tax advance payments.</span></span>

    -   <span data-ttu-id="c6114-339">**Годы** — создание журнала для расчета годового транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-339">**Years** – Generate a journal for the annual transport tax calculation.</span></span>

5.  <span data-ttu-id="c6114-340">В поле **Номер периода**, если вы установили **Квартал** в поле **Типы периодов**, введите номер квартала.</span><span class="sxs-lookup"><span data-stu-id="c6114-340">In the **Period number** field, if you selected **Quarter** in the **Period types** field, enter the number of the quarter.</span></span> <span data-ttu-id="c6114-341">Если вы выбрали **Годы**, введите **1**.</span><span class="sxs-lookup"><span data-stu-id="c6114-341">If you selected **Years**, enter **1**.</span></span>

6.  <span data-ttu-id="c6114-342">В полях **Годы** введите отчетный год в формате *ГГГГ*.</span><span class="sxs-lookup"><span data-stu-id="c6114-342">In the **Years** fields, enter the reporting year in *YYYY* format.</span></span>

7.  <span data-ttu-id="c6114-343">Выберите **ОК**, чтобы создать журнал.</span><span class="sxs-lookup"><span data-stu-id="c6114-343">Select **OK** to create the journal.</span></span>

8.  <span data-ttu-id="c6114-344">Выберите **Строки**, чтобы создать строки в периодическом журнала регистров.</span><span class="sxs-lookup"><span data-stu-id="c6114-344">Select **Lines** to create lines in the periodic register journal.</span></span>

9.  <span data-ttu-id="c6114-345">Вы получаете сообщение о том, что "Журнал регистров не создавался.</span><span class="sxs-lookup"><span data-stu-id="c6114-345">You receive a message that states, "Register journal has not been created yet.</span></span> <span data-ttu-id="c6114-346">Создать журнал?"</span><span class="sxs-lookup"><span data-stu-id="c6114-346">Do you want create it?"</span></span> <span data-ttu-id="c6114-347">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="c6114-347">Select **Yes**.</span></span>

10. <span data-ttu-id="c6114-348">Проверьте налоговые регистры, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="c6114-348">Review the tax registers that are created.</span></span> <span data-ttu-id="c6114-349">Для транспортного налога создаются следующие регистры: **Транспортное средство — расчет налогов** и **Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-349">For transport tax, the following registers are created: **Vehicle – tax calculation** and **Transport tax**.</span></span>

11. <span data-ttu-id="c6114-350">Чтобы рассчитать конкретный налоговый регистр в журнале, выберите этот регистр, затем выберите **Рассчитать текущий**.</span><span class="sxs-lookup"><span data-stu-id="c6114-350">To calculate a specific tax register in the journal, select the register, and then select **Calculate current**.</span></span> <span data-ttu-id="c6114-351">Чтобы рассчитать все налоговые регистры в журнале, выберите **Рассчитать все**.</span><span class="sxs-lookup"><span data-stu-id="c6114-351">To calculate all tax registers in the journal, select **Calculate all**.</span></span>

12. <span data-ttu-id="c6114-352">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6114-352">Select **OK**.</span></span>

13. <span data-ttu-id="c6114-353">Выберите налоговый регистр, затем выберите **Строки регистра** для просмотра рассчитанных строк.</span><span class="sxs-lookup"><span data-stu-id="c6114-353">Select a tax register, and then select **Register lines** to review the calculated lines.</span></span>

14. <span data-ttu-id="c6114-354">Выберите **Печать** для печати строк налогового регистра в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c6114-354">Select **Print** to print the tax register lines in Microsoft Excel.</span></span>

15. <span data-ttu-id="c6114-355">Выберите **Сброс статуса**, чтобы сбросить статус рассчитанного регистра на **Не рассчитано**.</span><span class="sxs-lookup"><span data-stu-id="c6114-355">Select **Reset status** to reset the status of the calculated register to **Not calculated**.</span></span>

16. <span data-ttu-id="c6114-356">Когда закончите просмотр данных в налоговых регистрах, выберите флажок **Утверждено**, чтобы утвердить каждой регистр.</span><span class="sxs-lookup"><span data-stu-id="c6114-356">After you've finished reviewing the data in the tax registers, select the **Approved** check box to approve each register.</span></span>

17. <span data-ttu-id="c6114-357">В поле **Рабочий** просмотрите или измените код для утвердившего регистр сотрудника.</span><span class="sxs-lookup"><span data-stu-id="c6114-357">In the **Worker** field, view or change the code for the employee who approved the register.</span></span>

### <a name="create-and-calculate-corrective-tax-registers"></a><span data-ttu-id="c6114-358">Создание и расчет корректирующих налоговых регистров</span><span class="sxs-lookup"><span data-stu-id="c6114-358">Create and calculate corrective tax registers</span></span>

<span data-ttu-id="c6114-359">Если вы корректировали какие-либо данные транспортного средства за предыдущие периоды, следует создать корректирующие налоговые регистры, чтобы отразить исправленные суммы транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-359">If you've corrected any vehicle data for the previous periods, you should create corrective tax registers to reflect the corrected transport tax amounts.</span></span>

<span data-ttu-id="c6114-360">Чтобы создать корректирующие регистры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6114-360">To create corrective registers, follow these steps.</span></span>

1.  <span data-ttu-id="c6114-361">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="c6114-361">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="c6114-362">Выберите утвержденный журнал для периода, который необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="c6114-362">Select the approved journal for the period that must be corrected.</span></span>

3.  <span data-ttu-id="c6114-363">Выберите **Коррекция \> Исправления в текущем журнале**.</span><span class="sxs-lookup"><span data-stu-id="c6114-363">Select **Correction \> Corrections to current journal**.</span></span>

4.  <span data-ttu-id="c6114-364">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c6114-364">Select **New**.</span></span>

5.  <span data-ttu-id="c6114-365">В поле **Тип налога** выберите **Транспортный налог**, если необходимо исправить только регистры транспортного налога, или оставить это поле пустым, если необходимо исправить все налоговые регистры актива.</span><span class="sxs-lookup"><span data-stu-id="c6114-365">In the **Type of tax** field, either select **Transport tax** if you must correct only transport tax registers, or leave the field blank if you must correct all the asset's tax registers.</span></span>

6.  <span data-ttu-id="c6114-366">Убедитесь, что в полях **Типы периодов**, **Номер периода** и **Годы** заданы значения, которые подходят для периода регистра, который нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="c6114-366">Make sure that the **Period types**, **Period number**, and **Years** fields are set to values that are appropriate for the period of the register that you're correcting.</span></span>

7.  <span data-ttu-id="c6114-367">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6114-367">Select **OK**.</span></span>

8.  <span data-ttu-id="c6114-368">Создайте строки налогового регистра и рассчитайте и утвердите налоговые регистры, как описано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="c6114-368">Create tax register lines, and calculate and approve the tax registers as described in the previous procedure.</span></span>

<a name="generate-a-transport-tax-declaration"></a><span data-ttu-id="c6114-369">Создание налоговой декларации по налогу на транспортировку</span><span class="sxs-lookup"><span data-stu-id="c6114-369">Generate a transport tax declaration</span></span>
------------------------------------

### <a name="set-up-the-system-to-generate-a-transport-tax-declaration"></a><span data-ttu-id="c6114-370">Настройка системы для создания декларации по транспортному налогу</span><span class="sxs-lookup"><span data-stu-id="c6114-370">Set up the system to generate a transport tax declaration</span></span>

1.  <span data-ttu-id="c6114-371">В [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) в общей библиотеке активов загрузите последние версии конфигураций электронной отчетности (ER) для декларации налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="c6114-371">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the Shared asset library, download the latest versions of the Electronic reporting (ER) configurations for the assessed tax declaration.</span></span>

>   <span data-ttu-id="c6114-372">Например, для создания декларации по транспортному налогу за отчетный период 2019 года загрузите последнюю версию следующих конфигураций:</span><span class="sxs-lookup"><span data-stu-id="c6114-372">For example, to generate the transport tax declaration for the year 2019   reporting period, download the latest version of the following   configurations:</span></span>

-   <span data-ttu-id="c6114-373">Модель деклараций по ОС</span><span class="sxs-lookup"><span data-stu-id="c6114-373">Assets declarations model</span></span>

-   <span data-ttu-id="c6114-374">Сопоставление модели декларации транспортного налога</span><span class="sxs-lookup"><span data-stu-id="c6114-374">Transport tax declaration model mapping</span></span>

-   <span data-ttu-id="c6114-375">Формат декларации по транспортному налогу 5.05</span><span class="sxs-lookup"><span data-stu-id="c6114-375">Transport tax declaration format 5.05</span></span>

>   <span data-ttu-id="c6114-376">Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="c6114-376">For more information, see [Download Electronic reporting configurations from   Lifecycle   Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

1.  <span data-ttu-id="c6114-377">Можно передать параметры пакета управления данными для работы с декларацией транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-377">You can upload Data management package settings to work with the transport tax declaration.</span></span> <span data-ttu-id="c6114-378">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6114-378">Follow these steps:</span></span>

    -   <span data-ttu-id="c6114-379">В общей библиотеке активов LCS выберите **Пакет данных** как тип актива.</span><span class="sxs-lookup"><span data-stu-id="c6114-379">In the LCS Shared asset library, select **Data package** as the asset type.</span></span>

    -   <span data-ttu-id="c6114-380">Загрузите пакет с именем **RU Декларация транспортного налога v5.05 (2019)**.</span><span class="sxs-lookup"><span data-stu-id="c6114-380">Download the package that is named **RU Transport tax declaration v5.05 (2019)**.</span></span> <span data-ttu-id="c6114-381">Загружаемый файл называется **RU Transport tax declaration v5.05 (2019).zip**.</span><span class="sxs-lookup"><span data-stu-id="c6114-381">The file that is downloaded is named **RU Transport tax declaration v5.05 (2019).zip**.</span></span>

    -   <span data-ttu-id="c6114-382">В рабочей области **Управление данными** выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="c6114-382">In the **Data management** workspace, select **Import**.</span></span>

    -   <span data-ttu-id="c6114-383">В разделе **Сведения о задании** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c6114-383">In the **Job details** section, set the following values:</span></span>

        -   <span data-ttu-id="c6114-384">Введите имя должности.</span><span class="sxs-lookup"><span data-stu-id="c6114-384">Enter a name for the job.</span></span>

        -   <span data-ttu-id="c6114-385">В поле **Формат исходных данных** выберите **Пакет**.</span><span class="sxs-lookup"><span data-stu-id="c6114-385">In the **Source data format** field, select **Package**.</span></span>

    -   <span data-ttu-id="c6114-386">Выберите **Отправить** рядом с полем **Отправить файл данных**, затем выберите файл **RU Transport tax declaration v5.05 (2019).zip**, загруженный ранее.</span><span class="sxs-lookup"><span data-stu-id="c6114-386">Select **Upload** next to the **Upload data file** field, and then select the **RU Transport tax declaration v5.05 (2019).zip** file that you downloaded earlier.</span></span>

    -   <span data-ttu-id="c6114-387">После отправки информационных объектов выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="c6114-387">After the data entities are uploaded, select **Import**.</span></span>

2.  <span data-ttu-id="c6114-388">Выберите пункты **Налог \> Настройка \> Электронные сообщения \> Обработка электронного сообщения** и проверьте обработку импортированных электронных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c6114-388">Go to **Tax \> Setup \> Electronic messages \> Electronic message processing**, and validate the electronic message processing that is imported.</span></span> <span data-ttu-id="c6114-389">(Большая часть данных, которые были импортированы, представлена только на русском языке.)</span><span class="sxs-lookup"><span data-stu-id="c6114-389">(Most of the data that is imported is presented in the Russian language.)</span></span>

| <span data-ttu-id="c6114-390">**Processing**</span><span class="sxs-lookup"><span data-stu-id="c6114-390">**Processing**</span></span>            | <span data-ttu-id="c6114-391">**Код обработки**</span><span class="sxs-lookup"><span data-stu-id="c6114-391">**Processing code**</span></span>  | <span data-ttu-id="c6114-392">**Название**</span><span class="sxs-lookup"><span data-stu-id="c6114-392">**Name**</span></span>                                  |
|---------------------------|----------------------|-------------------------------------------|
| <span data-ttu-id="c6114-393">Декларация по транспортному налогу</span><span class="sxs-lookup"><span data-stu-id="c6114-393">Transport tax declaration</span></span> | <span data-ttu-id="c6114-394">ТрансНал 5.05 (2019)</span><span class="sxs-lookup"><span data-stu-id="c6114-394">ТрансНал 5.05 (2019)</span></span> | <span data-ttu-id="c6114-395">Декларация по транспортному налогу (2019)</span><span class="sxs-lookup"><span data-stu-id="c6114-395">Декларация по транспортному налогу (2019)</span></span> |

3.  <span data-ttu-id="c6114-396">Настройте формат электронной отчетности, который выполняется при создании бухгалтерской отчетности в электронном формате:</span><span class="sxs-lookup"><span data-stu-id="c6114-396">Set up the ER format that is run when accounting reporting is generated in electronic format:</span></span>

4.  <span data-ttu-id="c6114-397">Откройте **Налог \> Настройка \> Электронные сообщения \> Действия обработки сообщения**.</span><span class="sxs-lookup"><span data-stu-id="c6114-397">Go to **Tax \> Setup \> Electronic messages \> Message processing actions**.</span></span>

5.  <span data-ttu-id="c6114-398">Выберите действие **Создать TRAND 5.05**, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="c6114-398">Select the **Generate TRAND 5.05** action, and then select **Edit**.</span></span>

6.  <span data-ttu-id="c6114-399">Задайте для параметра **Показать диалоговое окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="c6114-399">Set the **Show dialog** option to **Yes**.</span></span>

7.  <span data-ttu-id="c6114-400">В поле **Сопоставление формата** выберите конфигурацию электронной отчетности **Формат декларации по транспортному налогу 5.05**, загруженную ранее.</span><span class="sxs-lookup"><span data-stu-id="c6114-400">In the **Format mapping** field, select the **Transport tax declaration format 5.05** ER configuration that you downloaded earlier.</span></span>

8.  <span data-ttu-id="c6114-401">Настройте код типа хозяйственной деятельности (ОКВЭД):</span><span class="sxs-lookup"><span data-stu-id="c6114-401">Set up the economic activity type code (OKVED):</span></span>

9.  <span data-ttu-id="c6114-402">Откройте **Налог \> Настройка \> Электронные сообщения \> Дополнительные поля**.</span><span class="sxs-lookup"><span data-stu-id="c6114-402">Go to **Tax \> Setup \> Electronic messages \> Additional fields**.</span></span>

10. <span data-ttu-id="c6114-403">Выберите запись **EconomicActivityTypeCode**.</span><span class="sxs-lookup"><span data-stu-id="c6114-403">Select the **EconomicActivityTypeCode** record.</span></span>

11. <span data-ttu-id="c6114-404">На экспресс-вкладке **Значение** выберите **Добавить**, затем введите значение кода.</span><span class="sxs-lookup"><span data-stu-id="c6114-404">On the **Value** FastTab, select **Add**, and then enter the value of the code.</span></span>

### <a name="generate-a-transport-tax-declaration"></a><span data-ttu-id="c6114-405">Создание налоговой декларации по налогу на транспортировку</span><span class="sxs-lookup"><span data-stu-id="c6114-405">Generate a transport tax declaration</span></span>

<span data-ttu-id="c6114-406">Прежде чем можно будет создать декларацию по транспортному налогу для налогового года, необходимо рассчитать регистры транспортного налога для того же года и для первого квартала, второго квартала и третьего квартала того же года.</span><span class="sxs-lookup"><span data-stu-id="c6114-406">Before you can generate the transport tax declaration for a tax year, you must calculate the transport tax registers for the same year, and for the first quarter, second quarter, and third quarter of the same year.</span></span> <span data-ttu-id="c6114-407">Сумма авансового платежа для транспортного налога, экспортированная в декларацию по транспортному налогу, берется из налоговых регистров, рассчитанных для первого квартала, второго квартала и третьего квартала.</span><span class="sxs-lookup"><span data-stu-id="c6114-407">The advance payment amount for transport tax that is exported in the transport tax declaration is taken from the tax registers that were calculated for the first quarter, second quarter, and third quarter.</span></span>

1.  <span data-ttu-id="c6114-408">Откройте **Налог \> Запросы и отчеты \> Электронные сообщения \> Электронные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="c6114-408">Go to **Tax \> Inquiries and reports \> Electronic messages \> Electronic messages**.</span></span>

2.  <span data-ttu-id="c6114-409">Выберите формат отчета, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="c6114-409">Select the report format to generate.</span></span>

    <span data-ttu-id="c6114-410">Например, чтобы создать декларацию по транспортному налогу в формате XML за 2019 год, выберите **ТрансНал 5.05 (2019)**.</span><span class="sxs-lookup"><span data-stu-id="c6114-410">For example, to generate a transport tax declaration in XML format for the year 2019, select **ТрансНал 5.05 (2019)**.</span></span>

3.  <span data-ttu-id="c6114-411">На экспресс-вкладке **Сообщения** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c6114-411">On the **Messages** FastTab, select **New**.</span></span>

4.  <span data-ttu-id="c6114-412">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6114-412">In the **Run processing** dialog box, select **OK**.</span></span>

5.  <span data-ttu-id="c6114-413">Выберите созданную строку сообщения и введите описание.</span><span class="sxs-lookup"><span data-stu-id="c6114-413">Select the message line that is created, and enter a description.</span></span>

6.  <span data-ttu-id="c6114-414">Введите начальную и конечную дату для отчета.</span><span class="sxs-lookup"><span data-stu-id="c6114-414">Enter a start date and end date for the report.</span></span>

    <span data-ttu-id="c6114-415">Для создания декларации по транспортному налогу введите годовой период.</span><span class="sxs-lookup"><span data-stu-id="c6114-415">To generate a transport tax declaration, enter the year period.</span></span> <span data-ttu-id="c6114-416">Например, для 2019 года введите **01.01.2019** в поле **Начальная дата** и **31.12.2019** в поле **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="c6114-416">For example, for the year 2019, enter **01.01.2019** in the **From date** field and **31.12.2019** in the **To date** field.</span></span>

7.  <span data-ttu-id="c6114-417">Необязательно: для корректирующей декларации на экспресс-вкладке **Дополнительные поля сообщения** в строке для поля **CorrectionNumber** в поле **Значение поля** введите число корректировки для корректирующей декларации.</span><span class="sxs-lookup"><span data-stu-id="c6114-417">Optional: For a corrective declaration, on the **Message additional fields** FastTab, on the line for the **CorrectionNumber** field, in the **Field value** field, enter the number of the correction.</span></span>

8.  <span data-ttu-id="c6114-418">На экспресс-вкладке **Сообщения** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="c6114-418">On the **Messages** FastTab, select **Update status**.</span></span>

9.  <span data-ttu-id="c6114-419">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6114-419">In the **Run processing** dialog box, select **OK**.</span></span>

10. <span data-ttu-id="c6114-420">Проверьте, что статус сообщения изменился на **Готово к формированию**.</span><span class="sxs-lookup"><span data-stu-id="c6114-420">Validate that the message status has been changed to **Ready to generate**.</span></span>

11. <span data-ttu-id="c6114-421">На экспресс-вкладке **Сообщения** выберите **Создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="c6114-421">On the **Messages** FastTab, select **Generate report**.</span></span>

12. <span data-ttu-id="c6114-422">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Параметр** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c6114-422">In the **Electronic reporting parameters** dialog box, on the **Parameter** FastTab, set the following values.</span></span>

| <span data-ttu-id="c6114-423">**Поле**</span><span class="sxs-lookup"><span data-stu-id="c6114-423">**Field**</span></span>                                                        | <span data-ttu-id="c6114-424">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6114-424">**Description**</span></span>                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6114-425">По месту</span><span class="sxs-lookup"><span data-stu-id="c6114-425">At place of</span></span>                                                      | <span data-ttu-id="c6114-426">Выберите место, где предоставляется декларация: **Расположение транспортного средства** или **Регистрация крупнейшего налогоплательщика**.</span><span class="sxs-lookup"><span data-stu-id="c6114-426">Select the place where the declaration is submitted: **Vehicle location** or **Registration of the largest taxpayer**.</span></span>                      |
| <span data-ttu-id="c6114-427">Номер корректировки</span><span class="sxs-lookup"><span data-stu-id="c6114-427">Correction number</span></span>                                                | <span data-ttu-id="c6114-428">Введите количество корректировки, если оно не было указано на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="c6114-428">Enter the number of the correction if you didn't specify it in step 7.</span></span>                                                                      |
| <span data-ttu-id="c6114-429">Тип подписавшей стороны</span><span class="sxs-lookup"><span data-stu-id="c6114-429">Signatory type</span></span>                                                   | <span data-ttu-id="c6114-430">Выберите лицо, которое подписывает учетную отчетность: **Налогоплательщик** или **Представитель**.</span><span class="sxs-lookup"><span data-stu-id="c6114-430">Select the person who signs the accounting reporting: **Taxpayer** or **Representative**.</span></span>                                                   |
| <span data-ttu-id="c6114-431">Имя подписавшего, отчество подписавшего, фамилия подписавшего</span><span class="sxs-lookup"><span data-stu-id="c6114-431">Signatory first name, Signatory middle name, Signatory last name</span></span> | <span data-ttu-id="c6114-432">Введите полное имя подписавшего.</span><span class="sxs-lookup"><span data-stu-id="c6114-432">Enter the full name of the signatory.</span></span>                                                                                                       |
| <span data-ttu-id="c6114-433">Компания-представитель</span><span class="sxs-lookup"><span data-stu-id="c6114-433">Representative company</span></span>                                           | <span data-ttu-id="c6114-434">Если выбран тип подписи **Представитель** и представитель является организацией, введите название организации.</span><span class="sxs-lookup"><span data-stu-id="c6114-434">If you selected **Representative** as the signatory type, and if the representative is an organization, enter the name of the organization.</span></span> |
| <span data-ttu-id="c6114-435">Документ представителя</span><span class="sxs-lookup"><span data-stu-id="c6114-435">Representative document</span></span>                                          | <span data-ttu-id="c6114-436">Если вы установили **Представитель** в качестве типа подписи, введите документ, подтверждающий полномочия представителя.</span><span class="sxs-lookup"><span data-stu-id="c6114-436">If you selected **Representative** as the signatory type, enter the document that confirms the representative's authority.</span></span>                  |

13. <span data-ttu-id="c6114-437">На первой экспресс-вкладке **Записи для добавления** примените фильтр для отдельных подразделений, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="c6114-437">On the first **Records to include** FastTab, apply a filter for separate divisions, if this type of filter is applicable.</span></span> <span data-ttu-id="c6114-438">В этом случае декларации будут создаваться только для выбранных отдельных подразделений.</span><span class="sxs-lookup"><span data-stu-id="c6114-438">In this case, declarations will be generated only for the selected separate divisions.</span></span>

14. <span data-ttu-id="c6114-439">На второй экспресс-вкладке **Записи для добавления** примените фильтр для налоговых органов, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="c6114-439">On the second **Records to include** FastTab, apply a filter for tax authorities, if this type of filter is applicable.</span></span> <span data-ttu-id="c6114-440">В этом случае декларации будут создаваться только для выбранных налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="c6114-440">In this case, declarations will be generated only for the selected tax authorities.</span></span>

15. <span data-ttu-id="c6114-441">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6114-441">Select **OK**.</span></span>

>   <span data-ttu-id="c6114-442">При создании отчета статус сообщения изменяется на **Создано**.</span><span class="sxs-lookup"><span data-stu-id="c6114-442">When the report is generated, the status of the message is changed to **Generated**.</span></span> <span data-ttu-id="c6114-443">При возникновении ошибки во время создания статус изменяется на **Техническая ошибка**.</span><span class="sxs-lookup"><span data-stu-id="c6114-443">If an error occurs during generation, the status is changed to **Technical error**.</span></span>

1.  <span data-ttu-id="c6114-444">На экспресс-вкладке **Журнал действий** просмотрите все действия пользователя для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="c6114-444">On the **Action log** FastTab, review all user actions for the current message.</span></span>

2.  <span data-ttu-id="c6114-445">Для просмотра созданного отчета выберите кнопку **Вложения** (символ скрепки) в верхнем правом углу страницы, затем выберите **Открыть** для просмотра файла.</span><span class="sxs-lookup"><span data-stu-id="c6114-445">To review the report that is generated, select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, and then select **Open** to view the file.</span></span>

<span data-ttu-id="c6114-446">Необходимо также вручную отправить созданный файл в специальное программное обеспечение независимых разработчиков для предварительного просмотра данных, обновления данных и передачи файлов декларации по транспортному налогу в налоговые органы по каналам связи.</span><span class="sxs-lookup"><span data-stu-id="c6114-446">You must also manually upload the generated file to the special third-party software for data preview, data updates, and transfer of the transport tax declaration files to the tax authorities through the communication channels.</span></span>

<a name="create-and-post-transport-tax-ledger-transactions"></a><span data-ttu-id="c6114-447">Создание и разноска проводок ГК по транспортному налогу</span><span class="sxs-lookup"><span data-stu-id="c6114-447">Create and post transport tax ledger transactions</span></span>
-------------------------------------------------

<span data-ttu-id="c6114-448">После расчета и утверждения налоговых регистров и создания декларации по транспортному налогу можно создать проводки для начисления транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-448">After you've calculated and approved tax registers, and generated a transport tax declaration, you can create transactions for transport tax accruals.</span></span>
<span data-ttu-id="c6114-449">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6114-449">Following these steps.</span></span>

1.  <span data-ttu-id="c6114-450">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="c6114-450">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="c6114-451">Выберите журнал, затем выберите **Журнал ГК \> Транспортный налог**.</span><span class="sxs-lookup"><span data-stu-id="c6114-451">Select the journal, and then select **Ledger journal \> Transport tax**.</span></span>

3.  <span data-ttu-id="c6114-452">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c6114-452">Select **New**.</span></span>

4.  <span data-ttu-id="c6114-453">В поле **Наименование** выберите наименование журнала транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="c6114-453">In the **Name** field, select the name of the transport tax journal.</span></span>

5.  <span data-ttu-id="c6114-454">Выберите **Строки** для просмотра строк журнала, которые содержат проводки начисления транспортного налога, которые были созданы на основании данных налогового регистра и настроек параметров для основных средств.</span><span class="sxs-lookup"><span data-stu-id="c6114-454">Select **Lines** to view the journal lines that have transport tax accrual transactions that were created based on the tax register data and the settings of Fixed assets parameters.</span></span>

6.  <span data-ttu-id="c6114-455">Проверьте и разнесите журнал.</span><span class="sxs-lookup"><span data-stu-id="c6114-455">Validate and post the journal.</span></span>
