---
title: Налоговая декларация по налогу на имущество (Россия)
description: В этой теме рассматривается настройка и использование деклараций по налогу на имущество для России.
author: ShylaThompson
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.search.industry: ''
ms.author: shylaw
ms.search.validFrom: 2019-05-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: dbddaade125f0a3985c202651316923d895c2e5a
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849317"
---
# <a name="assessed-tax-declaration-russia"></a><span data-ttu-id="651da-103">Налоговая декларация по налогу на имущество (Россия)</span><span class="sxs-lookup"><span data-stu-id="651da-103">Assessed tax declaration (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="651da-104">В соответствии с налоговым кодексом Российской Федерации объекты недвижимости облагаются налогом на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-104">According to the tax code of the Russian Federation, realty assetsare subject to assessed tax.</span></span>

<span data-ttu-id="651da-105">Налоговый период налога на имущество равен одному году.</span><span class="sxs-lookup"><span data-stu-id="651da-105">The tax period for assessed tax is one year.</span></span> <span data-ttu-id="651da-106">Отчетные периоды: первый квартал (три месяца), второй квартал (шесть месяцев или полгода) и третий квартал (девять месяцев).</span><span class="sxs-lookup"><span data-stu-id="651da-106">The reporting periods are the first quarter (three months, the second quarter (six months or half year), and the third quarter (nine months).</span></span>

<span data-ttu-id="651da-107">В конце налогового периода компания должна подать декларацию по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-107">At the end of the tax period, a company must report an assessed tax declaration.</span></span> <span data-ttu-id="651da-108">В конце каждого отчетного периода компания должна подать декларацию по расчету авансовых платежей по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-108">At the end of each reporting period, the company must report an assessed tax advance payments calculation declaration.</span></span>

<span data-ttu-id="651da-109">Для большинства типов недвижимости декларация по налогу на имущество и расчет авансовых платежей по налогу на имущество должны подаваться в налоговые органы по месту нахождения недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-109">For most realty types, the assessed tax declaration and the assessed tax advance payments calculation should be submitted to the tax authority where the realty is located.</span></span> <span data-ttu-id="651da-110">В этом случае должен быть введен код **281** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="651da-110">In this case, the code **281** should be entered for the **at place of** attribute.</span></span> <span data-ttu-id="651da-111">Крупнейшие налогоплательщики могут подавать декларации в налоговые органы по месту регистрации в качестве крупнейшего налогоплательщика.</span><span class="sxs-lookup"><span data-stu-id="651da-111">The greatest taxpayers can submit declarations to the tax authority where the organization is registered as a greatest taxpayer.</span></span> <span data-ttu-id="651da-112">В этом случае должен быть введен код **215** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="651da-112">In this case, the code **215** should be entered for the **at place of** attribute.</span></span>

<span data-ttu-id="651da-113">Налоговая база для расчета налога на имущество является средней стоимостью за год объекта недвижимости или кадастровой стоимостью объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-113">The tax base for the calculation of assessed tax is either the annual average cost of the realty asset or the cadastral cost of the realty asset.</span></span>

<span data-ttu-id="651da-114">Среднегодовая стоимость рассчитывается как сумма значений остаточной стоимости для основного средства в виде недвижимости на первый день каждого месяца налогового (или учетного) периода и на первый день после налогового (или учетного) периода.</span><span class="sxs-lookup"><span data-stu-id="651da-114">The annual average cost is calculated as the sum of residual values (net book values) for the realty fixed asset on the first day of each month of the tax (or reporting) period, and on the first day of the month after the tax (or reporting) period.</span></span> <span data-ttu-id="651da-115">Сумма затем делится на количество месяцев в налоговом периоде плюс один.</span><span class="sxs-lookup"><span data-stu-id="651da-115">This sum is then divided by the number of months in the tax period plus one.</span></span> <span data-ttu-id="651da-116">Объекты недвижимости, которые облагаются налогом по среднегодовой стоимости, указываются в разделе 2 декларации по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-116">Realty assets that are taxed at the annual average cost are reported in section 2 of the assessed tax declaration.</span></span>

<span data-ttu-id="651da-117">Кадастровая стоимость определяется кадастровыми органами и должна указываться пользователем на карточке основного средства.</span><span class="sxs-lookup"><span data-stu-id="651da-117">The cadastral cost is defined by cadastral authorities and should be specified by the user on the fixed asset card.</span></span> <span data-ttu-id="651da-118">Объекты недвижимости, которые облагаются налогом по кадастровой стоимости, указываются в разделе 3 декларации по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-118">Realty assets that are taxed at the cadastral cost are reported in section 3 of the assessed tax declaration.</span></span>

<span data-ttu-id="651da-119">В этом раздел рассматривается, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="651da-119">This topic explains how to perform the following tasks:</span></span>

1.  [<span data-ttu-id="651da-120">Настройка налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-120">Set up assessed tax</span></span>](#set-up-assessed-tax)

2.  [<span data-ttu-id="651da-121">Создание объекта недвижимости и настройка параметров для расчета налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-121">Create a realty asset and set up parameters for assessed tax calculation</span></span>](#create-a-realty-asset-and-set-up-parameters-for-assessed-tax-calculation)

3.  [<span data-ttu-id="651da-122">Расчет регистров налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-122">Calculate assessed tax registers</span></span>](#calculate-assessed-tax-registers)

4.  [<span data-ttu-id="651da-123">Создание декларации по налогу на имущество и расчета авансовых платежей по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-123">Generate an assessed tax declaration and an assessed tax advance payments calculation</span></span>](#generate-an-assessed-tax-declaration-and-an-assessed-tax-advance-payments-calculation)

5.  [<span data-ttu-id="651da-124">Создание и разноска проводок ГК по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-124">Create and post assessed tax ledger transactions</span></span>](#generate-an-assessed-tax-declaration-and-an-assessed-tax-advance-payments-calculation)

## <a name="set-up-assessed-tax"></a><span data-ttu-id="651da-125">Настройка налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-125">Set up assessed tax</span></span>

<span data-ttu-id="651da-126">Ниже приведен обзор шагов по настройке налога на имущество:</span><span class="sxs-lookup"><span data-stu-id="651da-126">Here is an overview of the steps for setting up assessed tax:</span></span>

1.  [<span data-ttu-id="651da-127">Настройка кодов и ставок налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-127">Set up assessed tax codes and rates</span></span>](#set-up-assessed-tax-codes-and-rates)

2.  [<span data-ttu-id="651da-128">Настройка кодов бюджетного дохода для налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-128">Set up budget revenue codes for assessed tax</span></span>](#set-up-budget-revenue-codes-for-assessed-tax)

3.  [<span data-ttu-id="651da-129">Назначение кода бюджетного дохода налоговому коду</span><span class="sxs-lookup"><span data-stu-id="651da-129">Assign a budget revenue code to a sales tax code</span></span>](#assign-a-budget-revenue-code-a-to-sales-tax-code)

4.  [<span data-ttu-id="651da-130">Настройка методов для расчета базы налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-130">Set up methods for assessed tax base calculation</span></span>](#set-up-methods-of-assessed-tax-base-calculation)

5.  [<span data-ttu-id="651da-131">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="651da-131">Set up tax allowances</span></span>](#set-up-tax-allowances)

6.  [<span data-ttu-id="651da-132">Назначение налоговых льгот налоговому коду как уменьшение ставки налога и уменьшение суммы налога</span><span class="sxs-lookup"><span data-stu-id="651da-132">Assign tax allowances to a sales tax code as a reduction of the tax rate and a reduction of the tax amount</span></span>](#assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-and-a-reduction-of-the-tax-amount)

7.  [<span data-ttu-id="651da-133">Настройка кода территории (кода OKTMO) юридического лица</span><span class="sxs-lookup"><span data-stu-id="651da-133">Set up the territory code (OKTMO code) of the legal entity</span></span>](#set-up-the-territory-code-oktmo-code-of-the-legal-entity)

8.  [<span data-ttu-id="651da-134">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="651da-134">Set up tax authorities and related OKTMO codes</span></span>](#set-up-tax-authorities-and-related-oktmo-codes)

9.  [<span data-ttu-id="651da-135">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="651da-135">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>](#optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes)

10. [<span data-ttu-id="651da-136">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="651da-136">Set up the organization's locations and assign them to company divisions</span></span>](#set-up-the-organizations-locations-and-assign-them-to-company-divisions)

11. [<span data-ttu-id="651da-137">Настройка территорий для распределенных объектов недвижимости</span><span class="sxs-lookup"><span data-stu-id="651da-137">Set up territories for distributed realty assets</span></span>](#set-up-territories-for-distributed-realty-assets)

12. [<span data-ttu-id="651da-138">Настройка коэффициентов железнодорожных основных средств</span><span class="sxs-lookup"><span data-stu-id="651da-138">Set up railway assets factors</span></span>](#set-up-railway-assets-factors)

13. [<span data-ttu-id="651da-139">Настройка параметров ОС для разноски налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-139">Set up Fixed assets parameters for posting assessed tax</span></span>](#set-up-fixed-assets-parameters-for-posting-assessed-tax)

14. [<span data-ttu-id="651da-140">Настройка журнала для разноски налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-140">Set up the journal for posting assessed tax</span></span>](#set-up-the-journal-for-posting-assessed-tax)

15. [<span data-ttu-id="651da-141">Настройка групп разноски для разносок налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-141">Set up a posting group for assessed tax postings</span></span>](#set-up-a-posting-group-for-assessed-tax-postings)

### <a name="set-up-assessed-tax-codes-and-rates"></a><span data-ttu-id="651da-142">Настройка кодов и ставок налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-142">Set up assessed tax codes and rates</span></span>

1.  <span data-ttu-id="651da-143">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="651da-143">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>

2.  <span data-ttu-id="651da-144">Создайте налоговый код.</span><span class="sxs-lookup"><span data-stu-id="651da-144">Create a sales tax code.</span></span>

3.  <span data-ttu-id="651da-145">В поле **Тип налога** выберите **Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-145">In the **Type of tax** field, select **Assessed tax**.</span></span>

4.  <span data-ttu-id="651da-146">Укажите период сопоставления и группу разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="651da-146">Specify the settlement period and the ledger posting group.</span></span>

5.  <span data-ttu-id="651da-147">В области действий на вкладке **Налоговый код** в группе **Налоговый код** выберите **Значения**, чтобы открыть страницу **Значения налогового кода**.</span><span class="sxs-lookup"><span data-stu-id="651da-147">On the Action Pane, on the **Sales tax code** tab, in the **Sales tax code** group, select **Values** to open the **Sales tax code values** page.</span></span>

6.  <span data-ttu-id="651da-148">В поле **Значение** укажите ставку налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-148">In the **Value** field, specify the tax rate for the assessed tax.</span></span>

### <a name="set-up-budget-revenue-codes-for-assessed-tax"></a><span data-ttu-id="651da-149">Настройка кодов бюджетного дохода для налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-149">Set up budget revenue codes for assessed tax</span></span>

1.  <span data-ttu-id="651da-150">Выберите **Управление банком и кассовыми операциями \> Настройка \> Настройка платежного поручения \> Классификация доходов бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="651da-150">Go to **Cash and bank management \> Setup \> Payment order setup \> Budget revenue classification**.</span></span>

2.  <span data-ttu-id="651da-151">Создайте код доходов бюджета для налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-151">Create a budget revenue code for assessed tax.</span></span>

3.  <span data-ttu-id="651da-152">Установите флажок **ЕСГС**, чтобы указать, что код доходов бюджета относится к Единой системе газоснабжения (ЕСГС).</span><span class="sxs-lookup"><span data-stu-id="651da-152">Select the **SSGS** check box to indicate that the budget revenue code belongs to the Standard System of Gas Supply (SSGS).</span></span>

### <a name="assign-a-budget-revenue-code-a-to-sales-tax-code"></a><span data-ttu-id="651da-153">Назначение кода доходов бюджета налоговому коду</span><span class="sxs-lookup"><span data-stu-id="651da-153">Assign a budget revenue code a to sales tax code</span></span>

1.  <span data-ttu-id="651da-154">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="651da-154">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="651da-155">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="651da-155">Create a record.</span></span>

3.  <span data-ttu-id="651da-156">В поле **Тип налога** выберите **Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-156">In the **Type of tax** field, select **Assessed tax**.</span></span>

4.  <span data-ttu-id="651da-157">В поле **Код** выберите налоговый код налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-157">In the **Code** field, select the sales tax code for the assessed tax.</span></span>

5.  <span data-ttu-id="651da-158">В поле **Код доходов бюджета** выберите Код доходов бюджета, который соответствует выбранному налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="651da-158">In the **Budget revenue code** field, select the budget revenue code that corresponds to the selected sales tax code.</span></span>

### <a name="set-up-methods-of-assessed-tax-base-calculation"></a><span data-ttu-id="651da-159">Настройка методов расчета базы налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-159">Set up methods of assessed tax base calculation</span></span>

1.  <span data-ttu-id="651da-160">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Методы расчета базы налога на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-160">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Methods of assessed tax base calculation**.</span></span>

2.  <span data-ttu-id="651da-161">Для каждого кода вида основных средств укажите метод расчета базы налога на имущество (**Среднегодовая стоимость** или **Кадастровая стоимость**), как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="651da-161">For each asset kind code, specify the method of assessed tax base calculation (**Yearly average value** or **Cadastral value**), as shown in the following table.</span></span>

| <span data-ttu-id="651da-162">**Код**</span><span class="sxs-lookup"><span data-stu-id="651da-162">**Code**</span></span> | <span data-ttu-id="651da-163">**Описание**</span><span class="sxs-lookup"><span data-stu-id="651da-163">**Description**</span></span>                                                             | <span data-ttu-id="651da-164">**Метод расчета налоговой базы по состоянию на 1 января 2019 г.**</span><span class="sxs-lookup"><span data-stu-id="651da-164">**Method of tax base calculation as of January 1, 2019**</span></span> |
|----------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="651da-165">1</span><span class="sxs-lookup"><span data-stu-id="651da-165">1</span></span>        | <span data-ttu-id="651da-166">Единая система газоснабжения</span><span class="sxs-lookup"><span data-stu-id="651da-166">Unified gas supply system</span></span>                                                   | <span data-ttu-id="651da-167">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-167">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-168">2</span><span class="sxs-lookup"><span data-stu-id="651da-168">2</span></span>        | <span data-ttu-id="651da-169">Недвижимость, расположенным на разных территориях</span><span class="sxs-lookup"><span data-stu-id="651da-169">Realty that is located in different territories</span></span>                             | <span data-ttu-id="651da-170">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-170">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-171">3</span><span class="sxs-lookup"><span data-stu-id="651da-171">3</span></span>        | <span data-ttu-id="651da-172">Прочие</span><span class="sxs-lookup"><span data-stu-id="651da-172">Other</span></span>                                                                       | <span data-ttu-id="651da-173">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-173">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-174">4</span><span class="sxs-lookup"><span data-stu-id="651da-174">4</span></span>        | <span data-ttu-id="651da-175">Недвижимость, которая находится за границей, и налог за которую уплачивается за границей</span><span class="sxs-lookup"><span data-stu-id="651da-175">Realty that is located abroad and tax that is paid abroad</span></span>                   | <span data-ttu-id="651da-176">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-176">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-177">5</span><span class="sxs-lookup"><span data-stu-id="651da-177">5</span></span>        | <span data-ttu-id="651da-178">Недвижимость, которая находится в Калининградской особой зоне</span><span class="sxs-lookup"><span data-stu-id="651da-178">Realty that is located in the Kaliningrad special zone</span></span>                      | <span data-ttu-id="651da-179">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-179">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-180">7</span><span class="sxs-lookup"><span data-stu-id="651da-180">7</span></span>        | <span data-ttu-id="651da-181">Морские углеводородные поля</span><span class="sxs-lookup"><span data-stu-id="651da-181">Sea hydrocarbon fields</span></span>                                                      | <span data-ttu-id="651da-182">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-182">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-183">8</span><span class="sxs-lookup"><span data-stu-id="651da-183">8</span></span>        | <span data-ttu-id="651da-184">Газовые объекты</span><span class="sxs-lookup"><span data-stu-id="651da-184">Gas objects</span></span>                                                                 | <span data-ttu-id="651da-185">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-185">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-186">9</span><span class="sxs-lookup"><span data-stu-id="651da-186">9</span></span>        | <span data-ttu-id="651da-187">Железнодорожные объекты</span><span class="sxs-lookup"><span data-stu-id="651da-187">Railway objects</span></span>                                                             | <span data-ttu-id="651da-188">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-188">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-189">10</span><span class="sxs-lookup"><span data-stu-id="651da-189">10</span></span>       | <span data-ttu-id="651da-190">Силовые линии и трубопроводы</span><span class="sxs-lookup"><span data-stu-id="651da-190">Power lines and pipelines</span></span>                                                   | <span data-ttu-id="651da-191">Среднегодовая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-191">Yearly average value</span></span>                                     |
| <span data-ttu-id="651da-192">11</span><span class="sxs-lookup"><span data-stu-id="651da-192">11</span></span>       | <span data-ttu-id="651da-193">Недвижимость, которая облагается налогом по кадастровой стоимости</span><span class="sxs-lookup"><span data-stu-id="651da-193">Realty that is taxed at the cadastral cost</span></span>                                  | <span data-ttu-id="651da-194">Кадастровая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-194">Cadastral value</span></span>                                          |
| <span data-ttu-id="651da-195">12</span><span class="sxs-lookup"><span data-stu-id="651da-195">12</span></span>       | <span data-ttu-id="651da-196">Недвижимость зарубежного объекта, которая облагается налогом по кадастровой стоимости</span><span class="sxs-lookup"><span data-stu-id="651da-196">Realty of a foreign entity that is taxed at the cadastral cost</span></span>              | <span data-ttu-id="651da-197">Кадастровая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-197">Cadastral value</span></span>                                          |
| <span data-ttu-id="651da-198">13</span><span class="sxs-lookup"><span data-stu-id="651da-198">13</span></span>       | <span data-ttu-id="651da-199">Недвижимость, которая не учитывается в качестве основных средств и облагается налогом по кадастровой стоимости</span><span class="sxs-lookup"><span data-stu-id="651da-199">Realty that isn't accounted as fixed assets and taxed at the cadastral cost</span></span> | <span data-ttu-id="651da-200">Кадастровая стоимость</span><span class="sxs-lookup"><span data-stu-id="651da-200">Cadastral value</span></span>                                          |

### <a name="set-up-tax-allowances"></a><span data-ttu-id="651da-201">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="651da-201">Set up tax allowances</span></span>

1.  <span data-ttu-id="651da-202">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Налоговые льготы**.</span><span class="sxs-lookup"><span data-stu-id="651da-202">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Tax allowances**.</span></span>

2.  <span data-ttu-id="651da-203">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="651da-203">Create a record.</span></span>

3.  <span data-ttu-id="651da-204">Задайте значения для налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="651da-204">Set the values for the tax allowance.</span></span>

| <span data-ttu-id="651da-205">**Поле**</span><span class="sxs-lookup"><span data-stu-id="651da-205">**Field**</span></span>       | <span data-ttu-id="651da-206">**Описание**</span><span class="sxs-lookup"><span data-stu-id="651da-206">**Description**</span></span>                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651da-207">Привилегия</span><span class="sxs-lookup"><span data-stu-id="651da-207">Privilege</span></span>       | <span data-ttu-id="651da-208">Введите коды налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="651da-208">Enter the tax allowance code.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="651da-209">Тип налога</span><span class="sxs-lookup"><span data-stu-id="651da-209">Type of tax</span></span>     | <span data-ttu-id="651da-210">Выберите **Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-210">Select **Assessed tax**.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="651da-211">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="651da-211">Benefit type</span></span>    | <span data-ttu-id="651da-212">Выберите тип налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="651da-212">Select the type of tax allowance.</span></span> <span data-ttu-id="651da-213">Следующие значения применяются для налоговых льгот по налогу на имущество: **Освобождение от налога**, **Уменьшение налоговой базы**, **Снижение налоговой ставки** и **Уменьшение суммы налога**.</span><span class="sxs-lookup"><span data-stu-id="651da-213">The following values are applicable for assessed tax allowances: **Exemption from tax**, **Tax base reduction**, **Reduction of tax rate**, and **Reduction of tax amount**.</span></span> |
| <span data-ttu-id="651da-214">Название</span><span class="sxs-lookup"><span data-stu-id="651da-214">Name</span></span>            | <span data-ttu-id="651da-215">Введите название налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="651da-215">Enter the name of the tax allowance.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="651da-216">Величина льготы</span><span class="sxs-lookup"><span data-stu-id="651da-216">Allowance value</span></span> | <span data-ttu-id="651da-217">Определите значение налоговой льготы в зависимости от типа налоговой льготы, выбранного в поле **Тип льготы**:</span><span class="sxs-lookup"><span data-stu-id="651da-217">Define the tax allowance value, depending on type of tax allowance that you selected in the **Benefit type** field:</span></span>                                                                                            |

-   <span data-ttu-id="651da-218">**Освобождение от налога:** не определяйте величину льготы, поскольку освобождение от налога всегда берется 100 процентов, а сумма налога составляет 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="651da-218">**Exemption from tax:** Don't define the allowance value, because exemption from tax is always considered 100 percent, and the tax amount is 0 (zero).</span></span>

-   <span data-ttu-id="651da-219">**Уменьшение налоговой базы:** определите сумму, в местной валюте, на которую уменьшается сумма налоговой базы для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="651da-219">**Tax base reduction:** Define the amount, in the local currency, that is reducing the tax base amount for each asset.</span></span>

-   <span data-ttu-id="651da-220">**Снижение налоговой ставки:** задайте процент уменьшения налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="651da-220">**Reduction of tax rate:** Define the percentage of the tax rate reduction.</span></span>
    <span data-ttu-id="651da-221">Например, если налоговая ставка равна 10 процентам, а налоговая льгота равна 2 процентам, уменьшенная налоговая ставка равна 8 процентам.</span><span class="sxs-lookup"><span data-stu-id="651da-221">For example, if the tax rate is 10 percent, and the allowance value is 2 percent, the reduced tax rate is 8 percent.</span></span>

-   <span data-ttu-id="651da-222">**Уменьшение суммы налога:** определите сумму, в местной валюте, на которую уменьшается рассчитанная сумма налога для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="651da-222">**Reduction of tax amount:** Define the amount, in the local currency, that is reducing the calculated tax amount for each asset.</span></span>

### <a name="assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-and-a-reduction-of-the-tax-amount"></a><span data-ttu-id="651da-223">Назначение налоговых льгот налоговому коду как уменьшение ставки налога и уменьшение суммы налога</span><span class="sxs-lookup"><span data-stu-id="651da-223">Assign tax allowances to a sales tax code as a reduction of the tax rate and a reduction of the tax amount</span></span>

1.  <span data-ttu-id="651da-224">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="651da-224">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="651da-225">Выберите запись для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="651da-225">Select the record for the sales tax code.</span></span>

3.  <span data-ttu-id="651da-226">В полях **Льгота путем понижения ставки** и **Льгота путем уменьшения налога** выберите соответствующие налоговые льготы, если они применимы к налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="651da-226">In the **Allowance by reduction of rate** and **Allowance by reduction of tax** fields, select the appropriate tax allowances, if they are applicable to the sales tax code.</span></span>

### <a name="set-up-the-territory-code-oktmo-code-of-the-legal-entity"></a><span data-ttu-id="651da-227">Настройка кода территории (кода OKTMO) юридического лица</span><span class="sxs-lookup"><span data-stu-id="651da-227">Set up the territory code (OKTMO code) of the legal entity</span></span>

1.  <span data-ttu-id="651da-228">Перейдите в раздел **Управление организацией \> Организации \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="651da-228">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

2.  <span data-ttu-id="651da-229">На экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="651da-229">On the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

3.  <span data-ttu-id="651da-230">На странице **Управление адресами** на экспресс-вкладке **Регистрационный номер** создайте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-230">On the **Manage addresses** page, on the **Registration ID** FastTab, create a line.</span></span>

4.  <span data-ttu-id="651da-231">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="651da-231">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

>   <span data-ttu-id="651da-232">Если требуемый тип регистрации отсутствует в списке, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="651da-232">If the required registration type isn't listed, follow these steps:</span></span>

1.  <span data-ttu-id="651da-233">На странице **Типы регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Типы регистрации**) создайте тип регистрации.</span><span class="sxs-lookup"><span data-stu-id="651da-233">On the **Registration types** page (**Organization administration \> Global address book \> Registration types \> Registration types**), create a registration type.</span></span>

2.  <span data-ttu-id="651da-234">На странице **Категории регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Категории регистрации**) назначьте новый тип регистрации категории регистрации **ОКАТО**.</span><span class="sxs-lookup"><span data-stu-id="651da-234">On the **Registration categories** page (**Organization administration \> Global address book \> Registration types \> Registration categories**), assign the new registration type to the **RCOAD** registration category.</span></span>

3.  <span data-ttu-id="651da-235">В поле **Регистрационный номер** введите код OKTMO для местоположения юридического лица.</span><span class="sxs-lookup"><span data-stu-id="651da-235">In the field **Registration number**, enter the OKTMO code for the legal entity's location.</span></span>

### <a name="set-up-tax-authorities-and-related-oktmo-codes"></a><span data-ttu-id="651da-236">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="651da-236">Set up tax authorities and related OKTMO codes</span></span>

<span data-ttu-id="651da-237">Необходимо создать налоговые органы, в который вы должны подавать декларации по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-237">You must create the tax authorities that you're required to report assessed tax declarations to.</span></span>

1.  <span data-ttu-id="651da-238">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="651da-238">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax authorities**.</span></span>

2.  <span data-ttu-id="651da-239">Создайте налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="651da-239">Create a tax authority.</span></span>

3.  <span data-ttu-id="651da-240">Задайте поля **Налоговый орган** и **Название**.</span><span class="sxs-lookup"><span data-stu-id="651da-240">Set the **Authority** and **Name** fields.</span></span>

4.  <span data-ttu-id="651da-241">В поле **Код ГНИ** введите четырехзначный код налогового органа.</span><span class="sxs-lookup"><span data-stu-id="651da-241">In the **STI code** field, enter the four-digit code of the tax authority.</span></span>

5.  <span data-ttu-id="651da-242">В поле **Счет поставщика** выберите субъект счета поставщика, который связан с налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="651da-242">In the **Vendor account** field, select the vendor account party that is associated with the tax authority.</span></span>

6.  <span data-ttu-id="651da-243">Определите основной код OKTMO налогового органа для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="651da-243">Define the main OKTMO code of the tax authority on the vendor account:</span></span>

    1.  <span data-ttu-id="651da-244">В записи для счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="651da-244">In the record for the vendor account, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="651da-245">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-245">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="651da-246">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="651da-246">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="651da-247">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="651da-247">In the **Registration number** field, enter the OKTMO code.</span></span>

        <span data-ttu-id="651da-248">Примечание. Для объектов недвижимости, которые расположены в главном расположении организации, налоговый орган, в который подается отчет по налогу на имущество, определяется как в налоговый орган с кодом OKTMO, который совпадает с кодом OKTMO юридического лица.</span><span class="sxs-lookup"><span data-stu-id="651da-248">Note: For realty objects that are located at the organization's main location, the tax authority that assessed tax is reported to is defined as the tax authority that has an OKTMO code that matches the OKTMO code of the legal entity.</span></span>

### <a name="optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes"></a><span data-ttu-id="651da-249">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="651da-249">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>

<span data-ttu-id="651da-250">Если у организации имеются объекты недвижимости, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить подразделения компании.</span><span class="sxs-lookup"><span data-stu-id="651da-250">If the organization has realty objects that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up company divisions.</span></span>

1.  <span data-ttu-id="651da-251">Выберите **Управления организацией \> Настройка \> Обособленные подразделения**.</span><span class="sxs-lookup"><span data-stu-id="651da-251">Go to **Organization administration \> Setup \> Separate divisions**.</span></span>

2.  <span data-ttu-id="651da-252">Создание отдела компании.</span><span class="sxs-lookup"><span data-stu-id="651da-252">Create a company division.</span></span>

3.  <span data-ttu-id="651da-253">В поле **Код отдельного подразделения** введите идентификационный код для подразделения.</span><span class="sxs-lookup"><span data-stu-id="651da-253">In the **Separate division ID** field, enter the identification code for the division.</span></span>

4.  <span data-ttu-id="651da-254">В поле **Имя** введите имя подразделения.</span><span class="sxs-lookup"><span data-stu-id="651da-254">In the **Name** field, enter the name of the division.</span></span>

5.  <span data-ttu-id="651da-255">В поле **Счет поставщика** выберите номер счета поставщика, который связан с отделом.</span><span class="sxs-lookup"><span data-stu-id="651da-255">In the **Vendor account** field, select the vendor account number that is associated with the division.</span></span> <span data-ttu-id="651da-256">Если ни один счет поставщика недоступен для подразделения компании, необходимо создать счет.</span><span class="sxs-lookup"><span data-stu-id="651da-256">If there is no vendor account for the company division, create one.</span></span>

6.  <span data-ttu-id="651da-257">Определите код OKTMO подразделения компании для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="651da-257">Define the OKTMO code of the company division on the vendor account:</span></span>

    1.  <span data-ttu-id="651da-258">В записи счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="651da-258">In the vendor account record, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="651da-259">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-259">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="651da-260">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="651da-260">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="651da-261">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="651da-261">In the **Registration number** field, enter the OKTMO code.</span></span>

7.  <span data-ttu-id="651da-262">Повторите шаг 6, чтобы определить код КПП обособленного подразделения для счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="651da-262">Repeat step 6 to define the KPP code of the separate division on the vendor account.</span></span> <span data-ttu-id="651da-263">В поле **Тип регистрации** выберите тип регистрации, с которым связана категория регистрации **КПП**.</span><span class="sxs-lookup"><span data-stu-id="651da-263">In the **Registration type** field, select the registration type that is associated with the **KPP** registration category.</span></span>

### <a name="set-up-the-organizations-locations-and-assign-them-to-company-divisions"></a><span data-ttu-id="651da-264">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="651da-264">Set up the organization's locations and assign them to company divisions</span></span>

<span data-ttu-id="651da-265">Если у организации имеются объекты недвижимости, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить местоположения организации и назначить их подразделениям компании.</span><span class="sxs-lookup"><span data-stu-id="651da-265">If the organization has realty objects that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up organization locations and assign them to company divisions.</span></span>

1.  <span data-ttu-id="651da-266">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="651da-266">Go to **Fixed assets (Russia) \> Setup \> Location**.</span></span>

2.  <span data-ttu-id="651da-267">Выберите существующее местоположение или создайте новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="651da-267">Select an existing location, or create a new location.</span></span>

3.  <span data-ttu-id="651da-268">На экспресс-вкладке **Общие** в поле **Код отдельного подразделения** выберите подразделение компании, созданное в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="651da-268">On the **General** FastTab, in the **Separate division ID** field, select the company division that you created in the previous procedure.</span></span>

    <span data-ttu-id="651da-269">Примечание. Для объектов недвижимости, которые расположены на территориях, отличающихся от главного расположения организации, налоговый орган, в который подается отчет по налогу на имущество, определяется как в налоговый орган с кодом OKTMO, который совпадает с кодом OKTMO обособленного подразделения, связанного с местоположением недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-269">Note: For realty objects that are located in territories that differ from the organization's main location, the tax authority that assessed tax is reported to is defined as the tax authority that has an OKTMO code that matches the OKTMO code of the separate division that is associated with the realty location.</span></span> <span data-ttu-id="651da-270">Сведения о том, как связать основное средство с местоположением, см. в разделе [Указание местоположения недвижимости](#specify-the-location-of-the-realty) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="651da-270">For information about how to associate a fixed asset with a location, see the [Specify the location of the realty](#specify-the-location-of-the-realty) section later in this topic.</span></span>

    <span data-ttu-id="651da-271">Если поле **Код отдельного подразделения** пустое, местоположение совпадает с местоположением головного офиса организации.</span><span class="sxs-lookup"><span data-stu-id="651da-271">If the **Separate division ID** field is blank, the location is the same as the location of the organizationy's head office.</span></span>

### <a name="set-up-territories-for-distributed-realty-assets"></a><span data-ttu-id="651da-272">Настройка территорий для распределенных объектов недвижимости</span><span class="sxs-lookup"><span data-stu-id="651da-272">Set up territories for distributed realty assets</span></span>

<span data-ttu-id="651da-273">Если объект недвижимости распределен между несколькими территориями, сведения о нем должны подаваться под соответствующим кодом OKTMO.</span><span class="sxs-lookup"><span data-stu-id="651da-273">If a realty asset is distributed among several territories, it should be reported under the appropriate OKTMO code.</span></span> <span data-ttu-id="651da-274">Необходимо настроить территории распределения, назначить код OKTMO каждой территории и связать коды OKTMO с налоговыми органами.</span><span class="sxs-lookup"><span data-stu-id="651da-274">You should set up distribution territories, assign an OKTMO code to each territory, and associate the OKTMO codes with tax authorities.</span></span>

1.  <span data-ttu-id="651da-275">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Распределение**.</span><span class="sxs-lookup"><span data-stu-id="651da-275">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Distribution**.</span></span>

2.  <span data-ttu-id="651da-276">Создайте территорию.</span><span class="sxs-lookup"><span data-stu-id="651da-276">Create a territory.</span></span>

3.  <span data-ttu-id="651da-277">Задайте поля **Территория** и **Название**.</span><span class="sxs-lookup"><span data-stu-id="651da-277">Set the **Territory** and **Name** fields.</span></span>

4.  <span data-ttu-id="651da-278">Выберите налоговый код, который применяется к этой территории.</span><span class="sxs-lookup"><span data-stu-id="651da-278">Select the sales tax code that is applied in the territory.</span></span>

5.  <span data-ttu-id="651da-279">В поле **ОКАТО** выберите код ОКТМО территории.</span><span class="sxs-lookup"><span data-stu-id="651da-279">In the **RCOAD** field, select the OKTMO code of the territory.</span></span> <span data-ttu-id="651da-280">Для выбора доступны только коды OKTMO, связанные с налоговым органом налогового кода.</span><span class="sxs-lookup"><span data-stu-id="651da-280">Only OKTMO codes that are associated with the tax authority of the sales tax code are available for selection.</span></span> <span data-ttu-id="651da-281">Если нет доступных кодов OKTMO, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="651da-281">If no OKTMO code is available, follow these steps:</span></span>

    1.  <span data-ttu-id="651da-282">Выберите ссылку для налогового кода, чтобы открыть страницу **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="651da-282">Select the link for the sales tax code to open the **Sales tax codes** page.</span></span>

    2.  <span data-ttu-id="651da-283">Выберите ссылку для кода периода сопоставления налога, чтобы открыть страницу **Периоды сопоставления налогов**.</span><span class="sxs-lookup"><span data-stu-id="651da-283">Select the link for the settlement period code to open the **Sales tax settlement periods** page.</span></span>

    3.  <span data-ttu-id="651da-284">Выберите ссылку для кода налогового органа, чтобы открыть страницу **Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="651da-284">Select the link for the authority code to open the **Sales tax authorities** page.</span></span>

    4.  <span data-ttu-id="651da-285">В области действий выберите **Коды ОКАТО**.</span><span class="sxs-lookup"><span data-stu-id="651da-285">On the Action Pane, select **RCOAD codes**.</span></span>

    5.  <span data-ttu-id="651da-286">Создайте строки для кодов OKTMO, которые относятся к налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="651da-286">Create lines for the OKTMO codes that are related to the tax authority.</span></span>

>   <span data-ttu-id="651da-287">Можно также создать все коды OKTMO и присвоить код налоговому органу на странице **Коды ОКАТО** (**Налог \> Настройка \> Налог с продаж \> Коды ОКАТО**).</span><span class="sxs-lookup"><span data-stu-id="651da-287">Alternatively, create all the OKTMO codes, and assign a code to the tax   authority on the **RCOAD codes** page (**Tax \> Setup \> Sales tax \> RCOAD   codes**).</span></span>

### <a name="set-up-railway-assets-factors"></a><span data-ttu-id="651da-288">Настройка коэффициентов железнодорожных основных средств</span><span class="sxs-lookup"><span data-stu-id="651da-288">Set up railway assets factors</span></span>

<span data-ttu-id="651da-289">Если у организации имеются железные дороги, настройте коэффициент железнодорожных основных средств.</span><span class="sxs-lookup"><span data-stu-id="651da-289">If the organization has railways, set up the railway assets factors.</span></span>

1.  <span data-ttu-id="651da-290">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Коэффициенты железнодорожных основных средств**.</span><span class="sxs-lookup"><span data-stu-id="651da-290">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Railway assets factors**.</span></span>

2.  <span data-ttu-id="651da-291">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="651da-291">Select **New**.</span></span>

3.  <span data-ttu-id="651da-292">В поле **Номер налогового периода** введите год налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="651da-292">In the **Tax period number** field, enter the tax reporting year.</span></span>

4.  <span data-ttu-id="651da-293">В поле **Коэффициент** введите значение коэффициента железнодорожных ОС.</span><span class="sxs-lookup"><span data-stu-id="651da-293">In the **Factor** field, enter the railway factor value.</span></span>

5.  <span data-ttu-id="651da-294">Укажите дату вступления в силу и дату окончания срока действия для значения коэффициента.</span><span class="sxs-lookup"><span data-stu-id="651da-294">Specify effective and expiration dates for the factor value.</span></span>

### <a name="set-up-fixed-assets-parameters-for-posting-assessed-tax"></a><span data-ttu-id="651da-295">Настройка параметров ОС для разноски налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-295">Set up Fixed assets parameters for posting assessed tax</span></span>

1.  <span data-ttu-id="651da-296">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="651da-296">Go to **Fixed assets (Russia) \> Setup \> Parameters**.</span></span>

2.  <span data-ttu-id="651da-297">На вкладке **Номерные серии** для ссылки **Номер журнала регистров налога на имущество** выберите номерную серию для налогового регистра.</span><span class="sxs-lookup"><span data-stu-id="651da-297">On the **Number sequences** tab, for the **Assessed tax registers journal number** reference, select a number sequence for the tax register.</span></span>

3.  <span data-ttu-id="651da-298">На вкладке **Налоговая отчетность** в разделе **Налог на имущество** в поле **Код налога** выберите код налога по умолчанию для налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-298">On the **Tax reporting** tab, in the **Assessed tax** section, in the **Sales tax code** field, select the default sales tax code for assessed tax.</span></span>

4.  <span data-ttu-id="651da-299">В поле **Сжатие** выберите уровень сжатия для проводок налога на имущество:</span><span class="sxs-lookup"><span data-stu-id="651da-299">In the **Compression** field, select the level of compression for assessed tax transactions:</span></span>

-   <span data-ttu-id="651da-300">**Налог** — подробный журнал книги учета для проводок по налогу на имущество будет создаваться для каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="651da-300">**Tax** – A detailed ledger journal for assessed tax transactions will be created for each sales tax code.</span></span>

-   <span data-ttu-id="651da-301">**Итог** — журнал книги учета для проводок налога на имущество будет создаваться как одна строка с кодом налога по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="651da-301">**Total** – A ledger journal for assessed tax transactions will be created as one line that has the default sales tax code.</span></span>

1.  <span data-ttu-id="651da-302">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="651da-302">Close the page.</span></span>

### <a name="set-up-the-journal-for-posting-assessed-tax"></a><span data-ttu-id="651da-303">Настройка журнала для разноски налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-303">Set up the journal for posting assessed tax</span></span>

<span data-ttu-id="651da-304">Если проводки по налогу на имущество будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить журнал.</span><span class="sxs-lookup"><span data-stu-id="651da-304">If assessed tax transactions will be automatically created based on calculated tax registers, you should set up a journal.</span></span>

1.  <span data-ttu-id="651da-305">Перейдите в раздел **Главная книга \> Настройка журнала \> Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="651da-305">Go to **General ledger \> Journal setup \> Journal names**.</span></span>

2.  <span data-ttu-id="651da-306">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-306">Create a line.</span></span>

3.  <span data-ttu-id="651da-307">Задайте поля **Название** и **Серии ваучеров**.</span><span class="sxs-lookup"><span data-stu-id="651da-307">Set the **Name** and **Voucher series** fields.</span></span>

4.  <span data-ttu-id="651da-308">В поле **Тип журнала** выберите **Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-308">In the **Journal type** field, select **Assessed tax**.</span></span>

### <a name="set-up-a-posting-group-for-assessed-tax-postings"></a><span data-ttu-id="651da-309">Настройка групп разноски для разносок налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-309">Set up a posting group for assessed tax postings</span></span>

<span data-ttu-id="651da-310">Если проводки по налогу на имущество будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить группы разноски.</span><span class="sxs-lookup"><span data-stu-id="651da-310">If assessed tax transactions will be automatically created based on calculated tax registers, you should set up posting groups.</span></span>

1.  <span data-ttu-id="651da-311">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Группа разноски по налогам**.</span><span class="sxs-lookup"><span data-stu-id="651da-311">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Group of posting of taxes**.</span></span>

2.  <span data-ttu-id="651da-312">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-312">Create a line.</span></span>

3.  <span data-ttu-id="651da-313">В поле **Группа разноски ГК** выберите группу разноски ГК для налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-313">In the **Ledger posting group** field, select a ledger posting group for assessed tax.</span></span>

>   <span data-ttu-id="651da-314">Если в списке нет ни одной группы разноски ГК, создайте ее.</span><span class="sxs-lookup"><span data-stu-id="651da-314">If no ledger posting group is listed, create one.</span></span> <span data-ttu-id="651da-315">В поле **Исходящий налог** введите номер счета ГК для разноски налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-315">In the **Sales tax payable** field, enter the ledger account code for posting assessed tax.</span></span>

1.  <span data-ttu-id="651da-316">В поле **Счет для налогов ОС** выберите счет ГК для расходов по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-316">In the **Account for FA taxes** field, select a ledger account for the assessed tax expenses.</span></span>

2.  <span data-ttu-id="651da-317">Убедитесь, что в поле **Исходящий налог** установлено значение кода счета ГК, введенного для группы разноски главной книги на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="651da-317">Make sure that the **Sales tax payable** field is set to the ledger account code that you entered for the ledger posting group in step 3.</span></span>

<a name="create-a-realty-asset-and-set-up-parameters-for-assessed-tax-calculation"></a><span data-ttu-id="651da-318">Создание объекта недвижимости и настройка параметров для расчета налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-318">Create a realty asset and set up parameters for assessed tax calculation</span></span>
------------------------------------------------------------------------

<span data-ttu-id="651da-319">Ниже приведен обзор шагов для создания актива недвижимости и настройки параметров для расчета налога на имущество:</span><span class="sxs-lookup"><span data-stu-id="651da-319">Here is an overview of the steps for creating a realty asset and setting up parameters for assessed tax calculation:</span></span>

1.  [<span data-ttu-id="651da-320">Определение даты включения в налоговую базу для недвижимого актива</span><span class="sxs-lookup"><span data-stu-id="651da-320">Define the date of including in the tax base for a realty asset</span></span>](#define-the-date-of-including-in-the-tax-base-for-a-realty-asset)

2.  [<span data-ttu-id="651da-321">Регистрация недвижимости как основного средства</span><span class="sxs-lookup"><span data-stu-id="651da-321">Register realty as a fixed asset</span></span>](#register-realty-as-a-fixed-asset)

### <a name="define-the-date-of-including-in-the-tax-base-for-a-realty-asset"></a><span data-ttu-id="651da-322">Определение даты включения в налоговую базу для недвижимого актива</span><span class="sxs-lookup"><span data-stu-id="651da-322">Define the date of including in the tax base for a realty asset</span></span>

1.  <span data-ttu-id="651da-323">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="651da-323">Go to **Fixed assets (Russia) \> Setup \> Parameters**.</span></span>

2.  <span data-ttu-id="651da-324">На вкладке **Налоговая отчетность** в разделе **Налог на имущество** в поле **Дата включения в налоговую базу** укажите, когда объект недвижимости должен быть введен в налоговую базу налога на имущество:</span><span class="sxs-lookup"><span data-stu-id="651da-324">On the **Tax reporting** tab, in the **Assessed tax** section, in the **Date of including in the tax base** field, specify when the realty asset should be entered in the tax base of the assessed tax register:</span></span>

    -   <span data-ttu-id="651da-325">**Дата ввода в эксплуатацию** — дата, когда объект недвижимости введен в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="651da-325">**Putting into operation date** – The date when the realty asset is put into operation.</span></span>

    -   <span data-ttu-id="651da-326">**Дата регистрации** — дата регистрации объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-326">**Date of the registration** – The registration date of the realty asset.</span></span>

### <a name="register-realty-as-a-fixed-asset"></a><span data-ttu-id="651da-327">Регистрация недвижимости как основного средства</span><span class="sxs-lookup"><span data-stu-id="651da-327">Register realty as a fixed asset</span></span>

#### <a name="create-a-realty-fixed-asset-and-define-parameters-for-assessed-tax-calculation"></a><span data-ttu-id="651da-328">Создание основного средства недвижимости и определение параметров для расчета налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-328">Create a realty fixed asset and define parameters for assessed tax calculation</span></span>

1.  <span data-ttu-id="651da-329">Выберите **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="651da-329">Select **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="651da-330">Выберите существующее основное средство или создайте новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="651da-330">Select an existing fixed asset, or create a new fixed asset.</span></span>

3.  <span data-ttu-id="651da-331">На экспресс-вкладке **Общее** в поле **Тип** выберите **Недвижимость**.</span><span class="sxs-lookup"><span data-stu-id="651da-331">On the **General** FastTab, in the **Type** field, select **Realty**.</span></span>

4.  <span data-ttu-id="651da-332">В поле **Флаг владения** выберите, находится ли основное средство в собственности, операционном управлении, аренде или владении лица за пределами России.</span><span class="sxs-lookup"><span data-stu-id="651da-332">In the **Flag of ownership** field, select whether the fixed asset is owned, under operational management, leased, or owned by someone who is outside Russia.</span></span>

5.  <span data-ttu-id="651da-333">На экспресс-вкладке **Техническая информация** задайте поля **Дата регистрации** и **Дата удаления из регистра**.</span><span class="sxs-lookup"><span data-stu-id="651da-333">On the **Technical information** FastTab, set the **Date of the registration** and **Removal from the register date** fields.</span></span>

6.  <span data-ttu-id="651da-334">Укажите кадастровое значение для объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-334">Specify the cadastral value of the realty object.</span></span> <span data-ttu-id="651da-335">Если объект недвижимости является помещением внутри здания, также задайте поле **Кадастровая стоимость комнаты**.</span><span class="sxs-lookup"><span data-stu-id="651da-335">If the realty object is a room inside the building, also set the **Room cadastral value** field.</span></span>

7.  <span data-ttu-id="651da-336">На экспресс-вкладке **Налоговая отчетность** в разделе **Налог на имущество** в поле **Вид имущества** выберите код вида актива для объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-336">On the **Tax reporting** FastTab, in the **Assessed tax** section, in the **Asset kind** field, select the asset kind code of the realty.</span></span>

8.  <span data-ttu-id="651da-337">В поле **Налоговый код** выберите налоговый код для расчета налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-337">In the **Sales tax code** field, select the sales tax code for the assessed tax calculation.</span></span>

9.  <span data-ttu-id="651da-338">Если вы частично владеете основным средством, в полях **Числитель доли собственности** и **Знаменатель доли собственности** определите свою долю собственности в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="651da-338">If you partially own the fixed asset, in the **Owned share numerator** and **Owned share denominator** fields, define your ownership share as a simple fraction.</span></span>

10. <span data-ttu-id="651da-339">В поле **Код, по ОКОФ** укажите код из всероссийского классификатора основных средств.</span><span class="sxs-lookup"><span data-stu-id="651da-339">In the **Code by OKOF** field, specify the code from the all-Russia classifier of fixed assets.</span></span>

11. <span data-ttu-id="651da-340">В поле **Привилегия** укажите налоговую льготу типов **Освобождение от налога** и **Уменьшение налоговой базы**, если эти типы налоговых льгот применимы.</span><span class="sxs-lookup"><span data-stu-id="651da-340">In the **Privilege** field, specify the tax allowance of the **Exemption of tax** and **Tax base reduction** types, if these tax allowance types are applicable.</span></span>

12. <span data-ttu-id="651da-341">В поле **Налоговая база** проверьте метод расчета базы налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-341">In the **Tax base** field, review the method of assessed tax base calculation.</span></span>

13. <span data-ttu-id="651da-342">На экспресс-вкладке **Адрес** укажите адрес объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-342">On the **Address** FastTab, specify the address of the realty object.</span></span> <span data-ttu-id="651da-343">Если объект недвижимости не имеет кадастрового номера, адрес экспортируется в раздел 2.1 декларации налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-343">If the realty object doesn't have a cadastral number, the address is exported to section 2.1 of the assessed tax declaration.</span></span>

#### <a name="specify-the-location-of-the-realty"></a><span data-ttu-id="651da-344">Указание местоположения недвижимости</span><span class="sxs-lookup"><span data-stu-id="651da-344">Specify the location of the realty</span></span>

<span data-ttu-id="651da-345">По умолчанию объекты недвижимости считаются расположенными в месте расположения организации и отчет о них направляется налоговым органам на территории юридического лица.</span><span class="sxs-lookup"><span data-stu-id="651da-345">By default, realty objects are considered to be located at the organization's location and reported to the tax authority in the legal entity's territory.</span></span> <span data-ttu-id="651da-346">(Код налогового органа OKTMO соответствует коду OKTMO юридического лица, и объекты недвижимости включаются в отчет под тем же кодом OKTMO.)</span><span class="sxs-lookup"><span data-stu-id="651da-346">(The OKTMO code of the tax authority matches the OKTMO code of the legal entity, and realty objects are reported under the same OKTMO code.)</span></span>

<span data-ttu-id="651da-347">Если у организации есть объекты недвижимости, которые находятся на других территориях и зарегистрированы в других налоговых органах, необходимо указать местоположение объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-347">If the organization has realty objects that are located in different territories and registered in different tax authorities, you must specify the location of the realty asset.</span></span>

1.  <span data-ttu-id="651da-348">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="651da-348">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="651da-349">Выберите строку для объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-349">Select the line for the realty asset.</span></span>

3.  <span data-ttu-id="651da-350">В области действий на вкладке **Основные средства** в группе **История** выберите **Передача**.</span><span class="sxs-lookup"><span data-stu-id="651da-350">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Transfer**.</span></span>

4.  <span data-ttu-id="651da-351">Создайте строку и задайте поля **Дата** и **Новое местонахождение**.</span><span class="sxs-lookup"><span data-stu-id="651da-351">Create a line, and set the **Date** and **New location** fields.</span></span>

#### <a name="specify-the-distribution-for-a-realty-asset-that-is-located-in-several-territories"></a><span data-ttu-id="651da-352">Указание распределения для объекта недвижимости, расположенного на нескольких территориях</span><span class="sxs-lookup"><span data-stu-id="651da-352">Specify the distribution for a realty asset that is located in several territories</span></span>

1.  <span data-ttu-id="651da-353">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="651da-353">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="651da-354">Выберите строку для объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-354">Select the line for the realty asset.</span></span>

3.  <span data-ttu-id="651da-355">В области действий на вкладке **Основные средства** в группе **Распределение** выберите **Распределение**.</span><span class="sxs-lookup"><span data-stu-id="651da-355">On the Action Pane, on the **Fixed asset** tab, in the **Distribution** group, select **Distribution**.</span></span>

4.  <span data-ttu-id="651da-356">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-356">Create a line.</span></span>

5.  <span data-ttu-id="651da-357">В поле **Местоположение** выберите территорию.</span><span class="sxs-lookup"><span data-stu-id="651da-357">In the **Location** field, select a territory.</span></span>

6.  <span data-ttu-id="651da-358">Проверьте значения в полях **ОКАТО** и **Код налога**.</span><span class="sxs-lookup"><span data-stu-id="651da-358">Review the values in the **RCOAD** and **Sales tax code** fields.</span></span> <span data-ttu-id="651da-359">Эти значения автоматически вводятся из записи расположения территории.</span><span class="sxs-lookup"><span data-stu-id="651da-359">These values are automatically entered from the territory location record.</span></span>

7.  <span data-ttu-id="651da-360">В полях **Числитель доли распределения** и **Знаменатель доли распределения** определите долю распределения в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="651da-360">In the **Distribution share numerator** and **Distribution share denominator** fields, define the distribution share as a simple fraction.</span></span>
    <span data-ttu-id="651da-361">Эти поля будут использоваться для расчета стоимости недвижимости на территории.</span><span class="sxs-lookup"><span data-stu-id="651da-361">These fields will be used to calculate the realty's value in the territory.</span></span>

#### <a name="change-the-cadastral-cost-of-realty-that-is-taxed-according-to-cadastral-rules"></a><span data-ttu-id="651da-362">Изменение кадастровой стоимости недвижимости, которая облагается налогом в соответствии с кадастровыми правилами</span><span class="sxs-lookup"><span data-stu-id="651da-362">Change the cadastral cost of realty that is taxed according to cadastral rules</span></span>

<span data-ttu-id="651da-363">Кадастровая стоимость объекта недвижимости может измениться вследствие изменения качественных и количественных характеристик.</span><span class="sxs-lookup"><span data-stu-id="651da-363">The cadastral cost of a realty asset might change because of a change in qualitative and quantitative characteristics.</span></span> <span data-ttu-id="651da-364">Выполните следующие действия, чтобы записать изменения в кадастровой стоимости.</span><span class="sxs-lookup"><span data-stu-id="651da-364">Follow these steps to record the change in cadastral value.</span></span>

1.  <span data-ttu-id="651da-365">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="651da-365">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="651da-366">Выберите строку для объекта недвижимости.</span><span class="sxs-lookup"><span data-stu-id="651da-366">Select the line for the realty asset.</span></span>

3.  <span data-ttu-id="651da-367">В области действий на вкладке **Основные средства** в группе **История** выберите **Данные налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="651da-367">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Tax reporting data**.</span></span>

4.  <span data-ttu-id="651da-368">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="651da-368">Create a line.</span></span>

5.  <span data-ttu-id="651da-369">В поле **Период** укажите месяц, когда изменилась кадастровая стоимость.</span><span class="sxs-lookup"><span data-stu-id="651da-369">In the **Period** field, specify the month when the cadastral value is changing.</span></span>

6.  <span data-ttu-id="651da-370">В поле **Кадастровый номер** введите новый кадастровый номер.</span><span class="sxs-lookup"><span data-stu-id="651da-370">In the **Cadastral number** field, enter a new cadastral number.</span></span>

7.  <span data-ttu-id="651da-371">Если объект недвижимости является помещением в здании, задайте поле **Кадастровый номер помещения**.</span><span class="sxs-lookup"><span data-stu-id="651da-371">If the realty is a room in the building, set the **Room cadastral number** field.</span></span>

8.  <span data-ttu-id="651da-372">В полях **Числитель доли собственности** и **Знаменатель доли собственности** определите новую долю собственности в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="651da-372">In the **Owned share numerator** and **Owned share denominator** fields, define the new owned share as a simple fraction.</span></span>

>   <span data-ttu-id="651da-373">**Примечание**. Если это изменение будет первым изменением кадастровой стоимости, необходимо также создать строку для предыдущего значения, которое изначально было введено в запись основного средства.</span><span class="sxs-lookup"><span data-stu-id="651da-373">**Note**: If this change is the first change in cadastral value, you must   also create a line for the previous values that were originally entered in   the fixed asset record.</span></span>

>   <span data-ttu-id="651da-374">При создании строки для изменения кадастровой стоимости соответствующие поля в записи ОС больше нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="651da-374">When the line for the change in cadastral value is created, corresponding fields in the fixed asset record can no longer be edited.</span></span> <span data-ttu-id="651da-375">Они отображают фактическое значение из записи журнала данных налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="651da-375">They show the actual value from the tax reporting data history record.</span></span>

<a name="calculate-assessed-tax-registers"></a><span data-ttu-id="651da-376">Расчет регистров налога на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-376">Calculate assessed tax registers</span></span>
--------------------------------

<span data-ttu-id="651da-377">После завершения настройки, регистрации приобретения объектов недвижимости и настройки всех параметров объектов недвижимости для расчета налога на имущество, необходимо рассчитать регистры налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-377">After you've finished the setup, registered the acquisition of realty assets, and set up all realty asset parameters for assessed tax calculation, you must calculate assessed tax registers.</span></span> <span data-ttu-id="651da-378">Доступны следующие налоговые регистры:</span><span class="sxs-lookup"><span data-stu-id="651da-378">The following tax registers are available:</span></span>

-   <span data-ttu-id="651da-379">**Расчет затрат** — в зависимости от метода расчета налоговой базы, этот налоговый регистр рассчитывает либо значения остаточной стоимости каждого объекта недвижимости с первого дня каждого месяца в отчетном периоде или кадастровую стоимость каждого объекта за данный период.</span><span class="sxs-lookup"><span data-stu-id="651da-379">**Cost calculation** – Depending on the tax base calculation method, this tax register calculates either the net book values of each realty asset as of the first day of each month in the reporting period or the cadastral cost of each asset during that period.</span></span> <span data-ttu-id="651da-380">Эти суммы будут использоваться как основа для расчета налоговой базы для суммы налога, которая должна быть уплачена на территории, определяемой кодом OKTMO.</span><span class="sxs-lookup"><span data-stu-id="651da-380">These amounts will be used as the basis for the tax base calculation for the tax amount that must be paid in the territory that is identified by the OKTMO code.</span></span> <span data-ttu-id="651da-381">Регистр также отображает следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="651da-381">The register also shows the following information:</span></span>

>   <span data-ttu-id="651da-382">\- Доля собственности в случае частичной собственности на недвижимость</span><span class="sxs-lookup"><span data-stu-id="651da-382">\- The owned share, if the realty is partially owned</span></span>

>   <span data-ttu-id="651da-383">\- Доля распределенной собственности в случае распределенного объекта недвижимости (вид имущества</span><span class="sxs-lookup"><span data-stu-id="651da-383">\- The distributed property share, if the realty is distributed (asset kind</span></span>
>   02)

>   <span data-ttu-id="651da-384">\- Период владения и коэффициент в случае, если недвижимость была приобретена или продана в течение периода</span><span class="sxs-lookup"><span data-stu-id="651da-384">\- The ownership period and factor, in case the realty was acquired or sold   during the period</span></span>

>   <span data-ttu-id="651da-385">\- Период и коэффициент изменения стоимости, если кадастровая стоимость изменяется в течение периода</span><span class="sxs-lookup"><span data-stu-id="651da-385">\- The cost change period and factor, if the cadastral cost changes during   the period</span></span>

>   <span data-ttu-id="651da-386">\- Ставка налога на имущество, код доходов бюджета, код вида средства, код отдельного подразделения и расположение недвижимости, налоговый орган, в который будет подаваться отчет о недвижимости, дата приобретения недвижимости и код налоговой льготы через освобождение от налога или уменьшение налоговой базы</span><span class="sxs-lookup"><span data-stu-id="651da-386">\- The assessed tax rate, budget revenue code, asset kind code, separate   division ID, and location of the realty, the tax authority that the tax for   the realty will be reported to, the acquisition date of the realty, and the   code for tax allowance through exemption from tax or tax base reduction</span></span>

>   <span data-ttu-id="651da-387">**Итоги расчета остаточной стоимости** — этот регистр налога является техническим регистром, который рассчитывается на основе данных в налоговом регистре **Расчет затрат**.</span><span class="sxs-lookup"><span data-stu-id="651da-387">**Totals of net book value calculation** – This tax register is a technical register that is calculated based on the data in the **Cost calculation** tax register.</span></span> <span data-ttu-id="651da-388">В зависимости от метода расчета налоговой базы в нем отображается либо значения остаточной стоимости с учетом освобождения от налога на первый день каждого месяца отчетного периода или кадастровая стоимость основного средства с учетом освобождения от налога.</span><span class="sxs-lookup"><span data-stu-id="651da-388">Depending on the tax base calculation method, it shows either the tax-exempt net book values as of the first day of each month in the reporting period or the tax-exempt cadastral cost of the asset.</span></span>

-   <span data-ttu-id="651da-389">**Налог на имущество** — этот налоговый регистр является основой для декларации налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-389">**Assessed tax** – This tax register is the basis for an assessed tax declaration.</span></span> <span data-ttu-id="651da-390">Он рассчитывается на основе данных в налоговом регистре **Итоговые значения остаточной стоимости**.</span><span class="sxs-lookup"><span data-stu-id="651da-390">It's calculated based on the data in the **Totals of net book value** tax register.</span></span> <span data-ttu-id="651da-391">Для каждого кода OKTMO, кода доходов бюджета и объекта недвижимости в этом регистре отображаются следующие данные, которые должны быть учтены в декларации:</span><span class="sxs-lookup"><span data-stu-id="651da-391">For each OKTMO code, budget revenue code, and realty asset, this register shows the following data that must be reported in the declaration:</span></span>

-   <span data-ttu-id="651da-392">Средняя стоимость и средняя стоимость освобожденной недвижимости или кадастровая стоимость и кадастровая стоимость освобожденной недвижимости, в зависимости от метода расчета налоговой базы для объекта недвижимости и кода налоговой льготы через освобождения от налога или уменьшение налоговой базы</span><span class="sxs-lookup"><span data-stu-id="651da-392">The average cost and average cost of exempt realty, or the cadastral value and cadastral value of exempt realty, depending on the tax base calculation method of the realty, and the code for tax allowance through exemption from tax or tax base reduction</span></span>

-   <span data-ttu-id="651da-393">Доля собственности в случае частичной собственности на недвижимость</span><span class="sxs-lookup"><span data-stu-id="651da-393">The owned share, if the realty is partially owned</span></span>

-   <span data-ttu-id="651da-394">Доля распределенной собственности в случае распределенного объекта недвижимости</span><span class="sxs-lookup"><span data-stu-id="651da-394">The distributed property share, if the realty is distributed</span></span>

-   <span data-ttu-id="651da-395">Период владения и коэффициент в случае, если недвижимость была приобретена или продана в течение периода</span><span class="sxs-lookup"><span data-stu-id="651da-395">The ownership period and factor, if the realty is acquired or sold during the period</span></span>

-   <span data-ttu-id="651da-396">Период и коэффициент изменения стоимости, если кадастровая стоимость изменяется в течение периода</span><span class="sxs-lookup"><span data-stu-id="651da-396">The cost change period and factor, if the cadastral cost changes during the period</span></span>

-   <span data-ttu-id="651da-397">Ставка налога и код налоговой льготы через снижение налоговой ставки</span><span class="sxs-lookup"><span data-stu-id="651da-397">The tax rate and the code for tax allowance through reduction of the tax rate</span></span>

-   <span data-ttu-id="651da-398">Налоговая база, сумма налога (или сумма авансовых платежей), суммы аванса за предыдущие периоды и код и сумма налоговой льготы через уменьшение суммы налога</span><span class="sxs-lookup"><span data-stu-id="651da-398">The tax base, the tax amount (or advance payment amount), the advance amount for previous periods, and the code and amount for tax allowance through reduction of the tax amount</span></span>

-   <span data-ttu-id="651da-399">Сумма налога, уплачиваемая за пределами России (Это значение не вычисляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="651da-399">The tax amount that is paid outside Russia (This value isn't automatically calculated.</span></span> <span data-ttu-id="651da-400">Если оно необходимо, его следует вводить вручную.)</span><span class="sxs-lookup"><span data-stu-id="651da-400">If it's required, it must be manually entered.)</span></span>

>   <span data-ttu-id="651da-401">Чтобы рассчитать и утвердить регистры налога на имущество, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="651da-401">To calculate and approve assessed tax registers, follow these steps.</span></span>

1.  <span data-ttu-id="651da-402">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="651da-402">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="651da-403">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="651da-403">Select **New**.</span></span>

3.  <span data-ttu-id="651da-404">В поле **Тип налога** выберите **Налог на имущество** для создания журнала только для регистров налога на имущество или оставьте это поле пустым, чтобы создать журнал для всех налогов на ОС (налога на имущество, земельного налога и транспортного налога).</span><span class="sxs-lookup"><span data-stu-id="651da-404">In the **Type of tax** field, either select **Assessed tax** to create a journal for assessed tax registers only, or leave the field blank to create a journal for all the asset's taxes (assessed tax, land tax, transport tax).</span></span>

4.  <span data-ttu-id="651da-405">В поле **Типы периодов** выберите один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="651da-405">In the **Period types** field, select one of the following values:</span></span>

    -   <span data-ttu-id="651da-406">**Квартал** — создание журнала для расчета авансовых платежей по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-406">**Quarter** – Generate a journal for the assessed tax advance payments calculation.</span></span>

    -   <span data-ttu-id="651da-407">**Годы** — создание журнала для расчета годового налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-407">**Years** – Generate a journal for the annual assessed tax calculation.</span></span>

5.  <span data-ttu-id="651da-408">В поле **Номер периода**, если вы установили **Квартал** в поле **Типы периодов**, введите номер квартала.</span><span class="sxs-lookup"><span data-stu-id="651da-408">In the **Period number** field, if you selected **Quarter** in the **Period types** field, enter the number of the quarter.</span></span> <span data-ttu-id="651da-409">Если вы выбрали **Годы**, введите **1**.</span><span class="sxs-lookup"><span data-stu-id="651da-409">If you selected **Years**, enter **1**.</span></span>

6.  <span data-ttu-id="651da-410">В полях **Годы** введите отчетный год в формате *ГГГГ*.</span><span class="sxs-lookup"><span data-stu-id="651da-410">In the **Years** fields, enter the reporting year in the format *YYYY*.</span></span>

7.  <span data-ttu-id="651da-411">Выберите **ОК**, чтобы создать журнал.</span><span class="sxs-lookup"><span data-stu-id="651da-411">Select **OK** to create a journal.</span></span>

8.  <span data-ttu-id="651da-412">Выберите **Строки**, чтобы создать строки в периодическом журнала регистров.</span><span class="sxs-lookup"><span data-stu-id="651da-412">Select **Lines** to create lines in the periodic register journal.</span></span>

9.  <span data-ttu-id="651da-413">Вы получаете сообщение о том, что "Журнал регистров не создавался.</span><span class="sxs-lookup"><span data-stu-id="651da-413">You receive a message that states, "Register journal has not been created yet.</span></span> <span data-ttu-id="651da-414">Создать журнал?"</span><span class="sxs-lookup"><span data-stu-id="651da-414">Do you want create it?"</span></span> <span data-ttu-id="651da-415">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="651da-415">Select **Yes**.</span></span>

10. <span data-ttu-id="651da-416">Проверьте налоговые регистры, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="651da-416">Review the tax registers that are created.</span></span> <span data-ttu-id="651da-417">Для налога на имущество создаются следующие регистры: **Расчет затрат**, **Итоги расчета остаточной стоимости** и **Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-417">For assessed tax, the following registers are created: **Cost calculation**, **Totals of net book value calculation**, and **Assessed tax**.</span></span>

11. <span data-ttu-id="651da-418">Чтобы рассчитать конкретный налоговый регистр в журнале, выберите этот регистр, затем выберите **Рассчитать текущий**.</span><span class="sxs-lookup"><span data-stu-id="651da-418">To calculate a specific tax register in the journal, select the register, and then select **Calculate current**.</span></span> <span data-ttu-id="651da-419">Чтобы рассчитать все налоговые регистры в журнале, выберите **Рассчитать все**.</span><span class="sxs-lookup"><span data-stu-id="651da-419">To calculate all tax registers in the journal, select **Calculate all**.</span></span>

12. <span data-ttu-id="651da-420">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="651da-420">Select **OK**.</span></span>

13. <span data-ttu-id="651da-421">Выберите налоговый регистр, затем выберите **Строки регистра** для просмотра рассчитанных строк.</span><span class="sxs-lookup"><span data-stu-id="651da-421">Select a tax register, and then select **Register lines** to review the calculated lines.</span></span>

14. <span data-ttu-id="651da-422">Выберите **Печать** для печати строк налогового регистра в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="651da-422">Select **Print** to print the tax register lines in Microsoft Excel.</span></span>

15. <span data-ttu-id="651da-423">Выберите **Сброс статуса**, чтобы сбросить статус рассчитанного регистра на **Не рассчитано**.</span><span class="sxs-lookup"><span data-stu-id="651da-423">Select **Reset status** to reset the status of the calculated register to **Not calculated**.</span></span>

16. <span data-ttu-id="651da-424">Когда закончите просмотр данных в налоговых регистрах, выберите флажок **Утверждено**, чтобы утвердить каждой регистр.</span><span class="sxs-lookup"><span data-stu-id="651da-424">After you've finished reviewing the data in the tax registers, select the **Approved** check box to approve each register.</span></span>

17. <span data-ttu-id="651da-425">В поле **Рабочий** просмотрите или измените код утвердившего регистр сотрудника.</span><span class="sxs-lookup"><span data-stu-id="651da-425">In the **Worker** field, view or modify the code of the employee who approved the register.</span></span>

### <a name="create-and-calculate-corrective-tax-registers"></a><span data-ttu-id="651da-426">Создание и расчет корректирующих налоговых регистров</span><span class="sxs-lookup"><span data-stu-id="651da-426">Create and calculate corrective tax registers</span></span>

<span data-ttu-id="651da-427">Если вы корректировали какие-либо данные объекта недвижимости за предыдущие периоды, следует создать корректирующие налоговые регистры, чтобы отразить исправленные суммы налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-427">If you've corrected any realty asset data for the previous periods, you should create corrective tax registers to reflect the corrected assessed tax amounts.</span></span>

<span data-ttu-id="651da-428">Чтобы создать корректирующие регистры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="651da-428">To create corrective registers, follow these steps.</span></span>

1.  <span data-ttu-id="651da-429">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="651da-429">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="651da-430">Выберите утвержденный журнал для периода, который необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="651da-430">Select the approved journal for the period that must be corrected.</span></span>

3.  <span data-ttu-id="651da-431">Выберите **Коррекция \> Исправления в текущем журнале**.</span><span class="sxs-lookup"><span data-stu-id="651da-431">Select **Correction \> Corrections to current journal**.</span></span>

4.  <span data-ttu-id="651da-432">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="651da-432">Select **New**.</span></span>

5.  <span data-ttu-id="651da-433">В поле **Тип налога** выберите **Налог на имущество**, если необходимо исправить только регистры налога на имущество, или оставить это поле пустым, если необходимо исправить все налоговые регистры актива.</span><span class="sxs-lookup"><span data-stu-id="651da-433">In the **Type of tax** field, either select **Assessed tax** if you must correct only assessed tax registers, or leave the field blank if you must correct all the asset's tax registers.</span></span>

6.  <span data-ttu-id="651da-434">Убедитесь, что в полях **Типы периодов**, **Номер периода** и **Годы** заданы значения, которые подходят для периода регистра, который нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="651da-434">Make sure that the **Period types**, **Period number**, and **Years** fields are set to values that are appropriate for the period of the register that you're correcting.</span></span>

7.  <span data-ttu-id="651da-435">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="651da-435">Select **OK**.</span></span>

8.  <span data-ttu-id="651da-436">Создайте строки налогового регистра и рассчитайте и утвердите налоговые регистры, как описано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="651da-436">Create tax register lines, and calculate and approve the tax registers as described in the previous procedure.</span></span>

<a name="generate-an-assessed-tax-declaration-and-an-assessed-tax-advance-payments-calculation"></a><span data-ttu-id="651da-437">Создание декларации по налогу на имущество и расчета авансовых платежей по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-437">Generate an assessed tax declaration and an assessed tax advance payments calculation</span></span>
-------------------------------------------------------------------------------------

### <a name="set-up-the-system-to-generate-an-assessed-tax-declaration"></a><span data-ttu-id="651da-438">Настройка системы для создания декларации по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-438">Set up the system to generate an assessed tax declaration</span></span>

1.  <span data-ttu-id="651da-439">В [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) в общей библиотеке активов загрузите последние версии конфигураций электронной отчетности (ER) для декларации налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-439">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the Shared asset library, download the latest versions of the Electronic reporting (ER) configurations for the assessed tax declaration.</span></span>

>   <span data-ttu-id="651da-440">Например, для создания декларации по налогу на имущество за отчетный период 2019 года загрузите последние версии следующих конфигураций:</span><span class="sxs-lookup"><span data-stu-id="651da-440">For example, to generate the assessed tax declaration for the year 2019 reporting period, download the latest versions of the following configurations:</span></span>
> -   <span data-ttu-id="651da-441">Модель деклараций по ОС</span><span class="sxs-lookup"><span data-stu-id="651da-441">Assets declarations model</span></span>
> -  <span data-ttu-id="651da-442">Сопоставление модели декларации налога на собственность</span><span class="sxs-lookup"><span data-stu-id="651da-442">Property tax declaration model mapping</span></span>
> -   <span data-ttu-id="651da-443">Формат расчета авансовых платежей по налогу на собственность 5.05</span><span class="sxs-lookup"><span data-stu-id="651da-443">Property tax advance calculation format 5.05</span></span>
> -  <span data-ttu-id="651da-444">Формат декларации по налогу на собственность 5.05 Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="651da-444">Property tax declaration format 5.05 For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

1.  <span data-ttu-id="651da-445">Можно передать параметры пакета управления данными для работы с декларацией налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-445">You can upload Data management package settings to work with the assessed tax declaration.</span></span> <span data-ttu-id="651da-446">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="651da-446">Follow these steps:</span></span>

    -   <span data-ttu-id="651da-447">В общей библиотеке активов LCS выберите **Пакет данных** как тип актива.</span><span class="sxs-lookup"><span data-stu-id="651da-447">In the LCS Shared asset library, select **Data package** as the asset type.</span></span>

    -   <span data-ttu-id="651da-448">Загрузите пакет с именем **RU Декларация налога на собственность v5.05 (2019)**.</span><span class="sxs-lookup"><span data-stu-id="651da-448">Download the package that is named **RU Property tax declaration v5.05 (2019)**.</span></span> <span data-ttu-id="651da-449">Загружаемый файл называется **RU Property tax declaration v5.05 (2019).zip**.</span><span class="sxs-lookup"><span data-stu-id="651da-449">The file that is downloaded is named **RU Property tax declaration v5.05 (2019).zip**.</span></span>

    -   <span data-ttu-id="651da-450">В Microsoft Dynamics 365 for Finance and Operations в рабочей области **Управление данными** выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="651da-450">In Microsoft Dynamics 365 for Finance and Operations, in the **Data management** workspace, select **Import**.</span></span>

    -   <span data-ttu-id="651da-451">В разделе **Сведения о задании** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="651da-451">In the **Job details** section, set the following values:</span></span>

        -   <span data-ttu-id="651da-452">Введите имя должности.</span><span class="sxs-lookup"><span data-stu-id="651da-452">Enter a name for the job.</span></span>

        -   <span data-ttu-id="651da-453">В поле **Формат исходных данных** выберите **Пакет**.</span><span class="sxs-lookup"><span data-stu-id="651da-453">In the **Source data format** field, select **Package**.</span></span>

    -   <span data-ttu-id="651da-454">Выберите **Отправить** рядом с полем **Отправить файл данных**, затем выберите файл **RU Property tax declaration v5.05 (2019).zip**, загруженный ранее.</span><span class="sxs-lookup"><span data-stu-id="651da-454">Select **Upload** next to the **Upload data file** field, and then select the **RU Property tax declaration v5.05 (2019).zip** file that you downloaded earlier.</span></span>

    -   <span data-ttu-id="651da-455">После отправки информационных объектов выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="651da-455">After the data entities are uploaded, select **Import**.</span></span>

2.  <span data-ttu-id="651da-456">Выберите пункты **Налог \> Настройка \> Электронные сообщения \> Обработка электронного сообщения** и проверьте обработку импортированных электронных сообщений.</span><span class="sxs-lookup"><span data-stu-id="651da-456">Go to **Tax \> Setup \> Electronic messages \> Electronic message processing**, and validate the electronic message processing that is imported.</span></span> <span data-ttu-id="651da-457">(Большая часть данных, которые были импортированы, представлена только на русском языке.)</span><span class="sxs-lookup"><span data-stu-id="651da-457">(Most of the data that is imported is presented in the Russian language.)</span></span>

| <span data-ttu-id="651da-458">**Обработка**</span><span class="sxs-lookup"><span data-stu-id="651da-458">**Processing**</span></span>                            | <span data-ttu-id="651da-459">**Код обработки**</span><span class="sxs-lookup"><span data-stu-id="651da-459">**Processing code**</span></span>  | <span data-ttu-id="651da-460">**Название**</span><span class="sxs-lookup"><span data-stu-id="651da-460">**Name**</span></span>                                                |
|-------------------------------------------|----------------------|---------------------------------------------------------|
| <span data-ttu-id="651da-461">Декларация по имущественному налогу</span><span class="sxs-lookup"><span data-stu-id="651da-461">Property tax declaration</span></span>                  | <span data-ttu-id="651da-462">НалИмущД 5.05 (2019)</span><span class="sxs-lookup"><span data-stu-id="651da-462">НалИмущД 5.05 (2019)</span></span> | <span data-ttu-id="651da-463">Декларация по налогу на имущество(2019)</span><span class="sxs-lookup"><span data-stu-id="651da-463">Декларация по налогу на имущество(2019)</span></span>                 |
| <span data-ttu-id="651da-464">Расчет авансовых платежей по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-464">Property tax advance payments calculation</span></span> | <span data-ttu-id="651da-465">НалИмущР 5.05 (2019)</span><span class="sxs-lookup"><span data-stu-id="651da-465">НалИмущР 5.05 (2019)</span></span> | <span data-ttu-id="651da-466">Расчет авансовых платежей по налогу на имущество (2019)</span><span class="sxs-lookup"><span data-stu-id="651da-466">Расчет авансовых платежей по налогу на имущество (2019)</span></span> |

3.  <span data-ttu-id="651da-467">Настройте формат электронной отчетности, который выполняется при создании бухгалтерской отчетности в электронном формате.</span><span class="sxs-lookup"><span data-stu-id="651da-467">Set up the ER format that is run when accounting reporting is generated in electronic format.</span></span>

4.  <span data-ttu-id="651da-468">Откройте **Налог \> Настройка \> Электронные сообщения \> Действия обработки сообщения**.</span><span class="sxs-lookup"><span data-stu-id="651da-468">Go to **Tax \> Setup \> Electronic messages \> Message processing actions**.</span></span>

5.  <span data-ttu-id="651da-469">Выберите действие **Создать IMUD 5.05**, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="651da-469">Select the **Generate IMUD 5.05** action, and then select **Edit**.</span></span>

6.  <span data-ttu-id="651da-470">Задайте для параметра **Показать диалоговое окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="651da-470">Set the **Show dialog** option to **Yes**.</span></span>

7.  <span data-ttu-id="651da-471">В поле **Сопоставление формата** выберите конфигурацию электронной отчетности **Формат декларации налога на имущество 5.05**, загруженную ранее.</span><span class="sxs-lookup"><span data-stu-id="651da-471">In the **Format mapping** field, select the **Property tax declaration format 5.05** ER configuration that you downloaded earlier.</span></span>

8.  <span data-ttu-id="651da-472">Выберите действие **Создать IMUR 5.05**, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="651da-472">Select the **Generate IMUR 5.05** action, and then select **Edit**.</span></span>

9.  <span data-ttu-id="651da-473">Задайте для параметра **Показать диалоговое окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="651da-473">Set the **Show dialog** option to **Yes**.</span></span>

10. <span data-ttu-id="651da-474">В поле **Сопоставление формата** выберите конфигурацию электронной отчетности **Формат расчета авансовых платежей по налогу на имущество 5.05**, загруженную ранее.</span><span class="sxs-lookup"><span data-stu-id="651da-474">In the **Format mapping** field, select the **Property tax advance calculation format 5.05** ER configuration that you downloaded earlier.</span></span>

### <a name="generate-an-assessed-tax-declaration-and-an-assessed-tax-advance-payments-calculation"></a><span data-ttu-id="651da-475">Создание декларации по налогу на имущество и расчета авансовых платежей по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-475">Generate an assessed tax declaration and an assessed tax advance payments calculation</span></span>

<span data-ttu-id="651da-476">Чтобы можно было создать декларацию по налогу на имущество для налогового года, необходимо рассчитать регистр налога на имущество для этого года.</span><span class="sxs-lookup"><span data-stu-id="651da-476">Before you can generate the assessed tax declaration for a tax year, you must calculate the assessed tax register for the same year.</span></span>

<span data-ttu-id="651da-477">Чтобы можно было создать расчет авансовых платежей для отчетного периода (первый квартал, второй квартал или третий квартал), необходимо рассчитать регистр налога на имущество за этот же период.</span><span class="sxs-lookup"><span data-stu-id="651da-477">Before you can generate the advance payments calculation for a reporting period (first quarter, second quarter, or third quarter), you must calculate the assessed tax register for the same period.</span></span>

1.  <span data-ttu-id="651da-478">Откройте **Налог \> Запросы и отчеты \> Электронные сообщения \> Электронные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="651da-478">Go to **Tax \> Inquiries and reports \> Electronic messages \> Electronic messages**.</span></span>

2.  <span data-ttu-id="651da-479">Выберите формат отчета, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="651da-479">Select the report format to generate.</span></span>

    <span data-ttu-id="651da-480">Например, чтобы создать декларацию налога на имущество в формате XML за 2019 год, выберите **НалИмущД 5.05 (2019)**.</span><span class="sxs-lookup"><span data-stu-id="651da-480">For example, to generate an assessed tax declaration in XML format for the year 2019, select **НалИмущД 5.05 (2019)**.</span></span> <span data-ttu-id="651da-481">Чтобы создать расчет авансовых платежей по налогу на имущество в формате XML за 2019 год, выберите **НалИмущР 5.05 (2019)**.</span><span class="sxs-lookup"><span data-stu-id="651da-481">To generate an assessed tax advance payments calculation in XML format for the year 2019, select **НалИмущР 5.05 (2019)**.</span></span>

3.  <span data-ttu-id="651da-482">На экспресс-вкладке **Сообщения** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="651da-482">On the **Messages** FastTab, select **New**.</span></span>

4.  <span data-ttu-id="651da-483">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="651da-483">In the **Run processing** dialog box, select **OK**.</span></span>

5.  <span data-ttu-id="651da-484">Выберите созданную строку сообщения и введите описание.</span><span class="sxs-lookup"><span data-stu-id="651da-484">Select the message line that is created, and enter a description.</span></span>

6.  <span data-ttu-id="651da-485">Введите начальную и конечную дату для отчета.</span><span class="sxs-lookup"><span data-stu-id="651da-485">Enter a start date and end date for the report.</span></span>

    <span data-ttu-id="651da-486">Для создания декларации по налогу на имущество введите годовой период.</span><span class="sxs-lookup"><span data-stu-id="651da-486">To generate an assessed tax declaration, enter the year period.</span></span> <span data-ttu-id="651da-487">Например, для 2019 года введите **01.01.2019** в поле **Начальная дата** и **31.12.2019** в поле **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="651da-487">For example, for the year 2019, enter **01.01.2019** in the **From date** field and **31.12.2019** in the **To date** field.</span></span>

<span data-ttu-id="651da-488">Чтобы создать расчет авансовых платежей по налогу на имущество, введите квартальный период.</span><span class="sxs-lookup"><span data-stu-id="651da-488">To generate an assessed tax advance payments calculation, enter the quarter period.</span></span> <span data-ttu-id="651da-489">Например, для третьего квартала 2019 года введите **01.04.2019** в поле **Начальная дата** и **30.06.2019** в поле **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="651da-489">For example, for the third quarter of 2019, enter **01.04.2019** in the **From date** field and **30.06.2019** in the **To date**.</span></span>

1.  <span data-ttu-id="651da-490">Необязательно: на экспресс-вкладке **Дополнительные поля сообщения** в строке для поля **CorrectionNumber** в поле **Значение поля** введите число корректировки для корректирующей декларации. На экспресс-вкладке **Сообщения** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="651da-490">Optional: On the **Message additional fields** FastTab, on the line for the **CorrectionNumber** field, in the **Field value** field, enter the number of the correction for a corrective declaration On the **Messages** FastTab, select **Update status**.</span></span>

2.  <span data-ttu-id="651da-491">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="651da-491">In the **Run processing** dialog box, select **OK**.</span></span>

3.  <span data-ttu-id="651da-492">Проверьте, что статус сообщения изменился на **Готово к формированию**.</span><span class="sxs-lookup"><span data-stu-id="651da-492">Validate that the message status has been changed to **Ready to generate**.</span></span>

4.  <span data-ttu-id="651da-493">На экспресс-вкладке **Сообщения** выберите **Создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="651da-493">On the **Messages** FastTab, select **Generate report**.</span></span>

5.  <span data-ttu-id="651da-494">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Параметр** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="651da-494">In the **Electronic reporting parameters** dialog box, on the **Parameter** FastTab, set the following values.</span></span>

| <span data-ttu-id="651da-495">**Поле**</span><span class="sxs-lookup"><span data-stu-id="651da-495">**Field**</span></span>                                                        | <span data-ttu-id="651da-496">**Описание**</span><span class="sxs-lookup"><span data-stu-id="651da-496">**Description**</span></span>                                                                                                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651da-497">По месту</span><span class="sxs-lookup"><span data-stu-id="651da-497">At place of</span></span>                                                      | <span data-ttu-id="651da-498">Выберите место, где предоставляется декларация: **Расположение недвижимости**, **Регистрация крупнейшего налогоплательщика** или **Регистрация налогоплательщика**.</span><span class="sxs-lookup"><span data-stu-id="651da-498">Select the place where the declaration is submitted: **Realty location**, **Registration of the largest taxpayer**, or **Registration of the taxpayer**.</span></span> |
| <span data-ttu-id="651da-499">Номер корректировки</span><span class="sxs-lookup"><span data-stu-id="651da-499">Correction number</span></span>                                                | <span data-ttu-id="651da-500">Введите количество корректировки, если оно не было указано на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="651da-500">Enter the number of the correction if you didn't specify it in step 7.</span></span>                                                                                   |
| <span data-ttu-id="651da-501">Тип подписавшей стороны</span><span class="sxs-lookup"><span data-stu-id="651da-501">Signatory type</span></span>                                                   | <span data-ttu-id="651da-502">Выберите лицо, которое подписывает учетную отчетность: **Налогоплательщик** или **Представитель**.</span><span class="sxs-lookup"><span data-stu-id="651da-502">Select the person who signs the accounting reporting: **Taxpayer** or **Representative**.</span></span>                                                                |
| <span data-ttu-id="651da-503">Имя подписавшего, отчество подписавшего, фамилия подписавшего</span><span class="sxs-lookup"><span data-stu-id="651da-503">Signatory first name, Signatory middle name, Signatory last name</span></span> | <span data-ttu-id="651da-504">Введите полное имя подписавшего.</span><span class="sxs-lookup"><span data-stu-id="651da-504">Enter the full name of the signatory.</span></span>                                                                                                                    |
| <span data-ttu-id="651da-505">Компания-представитель</span><span class="sxs-lookup"><span data-stu-id="651da-505">Representative company</span></span>                                           | <span data-ttu-id="651da-506">Если выбран тип подписи **Представитель** и представитель является организацией, введите название организации.</span><span class="sxs-lookup"><span data-stu-id="651da-506">If you selected **Representative** as the signatory type, and if the representative is an organization, enter the name of the organization.</span></span>              |
| <span data-ttu-id="651da-507">Документ представителя</span><span class="sxs-lookup"><span data-stu-id="651da-507">Representative document</span></span>                                          | <span data-ttu-id="651da-508">Если вы установили **Представитель** в качестве типа подписи, введите документ, подтверждающий полномочия представителя.</span><span class="sxs-lookup"><span data-stu-id="651da-508">If you selected **Representative** as the signatory type, enter the document that confirms the representative's authority.</span></span>                               |

6.  <span data-ttu-id="651da-509">На первой экспресс-вкладке **Записи для добавления** примените фильтр для отдельных подразделений, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="651da-509">On the first **Records to include** FastTab, apply a filter for separate divisions, if this type of filter is applicable.</span></span> <span data-ttu-id="651da-510">В этом случае декларации будут создаваться только для выбранных отдельных подразделений.</span><span class="sxs-lookup"><span data-stu-id="651da-510">In this case, declarations will be generated only for the selected separate divisions.</span></span>

7.  <span data-ttu-id="651da-511">На второй экспресс-вкладке **Записи для добавления** примените фильтр для налоговых органов, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="651da-511">On the second **Records to include** FastTab, apply a filter for tax authorities, if this type of filter is applicable.</span></span> <span data-ttu-id="651da-512">В этом случае декларации будут создаваться только для выбранных налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="651da-512">In this case, declarations will be generated only for the selected tax authorities.</span></span>

8.  <span data-ttu-id="651da-513">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="651da-513">Select **OK**.</span></span>

>   <span data-ttu-id="651da-514">При создании отчета статус сообщения изменяется на **Создано**.</span><span class="sxs-lookup"><span data-stu-id="651da-514">When the report is generated, the status of the message is changed to **Generated**.</span></span> <span data-ttu-id="651da-515">При возникновении ошибки во время создания статус изменяется на **Техническая ошибка**.</span><span class="sxs-lookup"><span data-stu-id="651da-515">If an error occurs during generation, the status is changed to **Technical error**.</span></span>

1.  <span data-ttu-id="651da-516">На экспресс-вкладке **Журнал действий** просмотрите все действия пользователя для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="651da-516">On the **Action log** FastTab, review all user actions for the current message.</span></span>

2.  <span data-ttu-id="651da-517">Для просмотра созданного отчета выберите кнопку **Вложения** (символ скрепки) в верхнем правом углу страницы, затем выберите **Открыть** для просмотра файла.</span><span class="sxs-lookup"><span data-stu-id="651da-517">To review the report that is generated, select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, and then select **Open** to view the file.</span></span>

<span data-ttu-id="651da-518">Необходимо также вручную отправить созданный файл в специальное программное обеспечение независимых разработчиков для предварительного просмотра данных, обновления данных и передачи файлов декларации по налогу на имущество и расчета авансовых платежей по налогу на имущество в налоговые органы по каналам связи.</span><span class="sxs-lookup"><span data-stu-id="651da-518">You must also manually upload the generated file to the special third-party software for data preview, data updates, and transfer of the assessed tax declaration or assessed tax advance payments calculation files to the tax authorities through the communication channels.</span></span>

<a name="create-and-post-assessed-tax-ledger-transactions"></a><span data-ttu-id="651da-519">Создание и разноска проводок ГК по налогу на имущество</span><span class="sxs-lookup"><span data-stu-id="651da-519">Create and post assessed tax ledger transactions</span></span>
------------------------------------------------

<span data-ttu-id="651da-520">После расчета и утверждения налоговых регистров и создания декларации по налогу на имущество или расчета авансовых платежей по налогу на имущество создаются проводки для начисления налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-520">After you've calculated and approved tax registers, and generated an assessed tax declaration or an assessed tax advance payments calculation, you can create transactions for assessed tax accruals.</span></span> <span data-ttu-id="651da-521">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="651da-521">Following these steps.</span></span>

1.  <span data-ttu-id="651da-522">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="651da-522">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="651da-523">Выберите журнал, затем выберите **Журнал ГК \> Налог на имущество**.</span><span class="sxs-lookup"><span data-stu-id="651da-523">Select the journal, and then select **Ledger journal \> Assessed tax**.</span></span>

3.  <span data-ttu-id="651da-524">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="651da-524">Select **New**.</span></span>

4.  <span data-ttu-id="651da-525">В поле **Наименование** выберите наименование журнала налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="651da-525">In the **Name** field, select the name of the assessed tax journal.</span></span>

5.  <span data-ttu-id="651da-526">Выберите **Строки** для просмотра строк журнала, которые содержат проводки начисления налога на имущество, которые были созданы на основании данных налогового регистра и настроек параметров для основных средств.</span><span class="sxs-lookup"><span data-stu-id="651da-526">Select **Lines** to view the journal lines that have assessed tax accrual transactions that were created based on the tax register data and the settings of Fixed assets parameters.</span></span>

6.  <span data-ttu-id="651da-527">Проверьте и разнесите журнал.</span><span class="sxs-lookup"><span data-stu-id="651da-527">Validate and post the journal.</span></span>
