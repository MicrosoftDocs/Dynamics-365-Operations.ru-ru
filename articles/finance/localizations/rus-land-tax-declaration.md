---
title: Декларация по земельному налогу
description: В данном разделе содержится информация о декларации по земельному налогу для России.
author: anasyash
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-01-04
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b84e1a56a49f8c6a71f1280e4671aa6fab9f5c6b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893031"
---
# <a name="land-tax-declaration"></a><span data-ttu-id="83a80-103">Декларация по земельному налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-103">Land tax declaration</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="83a80-104">В соответствии с налоговым кодексом Российской Федерации земля облагается земельным налогом.</span><span class="sxs-lookup"><span data-stu-id="83a80-104">According to the tax code of the Russian Federation, land assets are subject to land tax.</span></span> <span data-ttu-id="83a80-105">Налоговый период земельного налога равен одному году.</span><span class="sxs-lookup"><span data-stu-id="83a80-105">The tax period for land tax is one year.</span></span> <span data-ttu-id="83a80-106">В конце налогового периода компания должна подать декларацию по земельному налогу.</span><span class="sxs-lookup"><span data-stu-id="83a80-106">At the end of the tax period, a company must report a land tax declaration.</span></span>

<span data-ttu-id="83a80-107">Декларацию по земельному налогу следует подавать в налоговый орган, где находится земля.</span><span class="sxs-lookup"><span data-stu-id="83a80-107">The land tax declaration should be submitted to the tax authority where the land is located.</span></span> <span data-ttu-id="83a80-108">В этом случае должен быть введен код **270** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="83a80-108">In this case, code **270** should be entered for the **at place of** attribute.</span></span> <span data-ttu-id="83a80-109">Однако крупнейшие налогоплательщики могут подавать декларации в налоговые органы по месту регистрации в качестве крупнейшего налогоплательщика.</span><span class="sxs-lookup"><span data-stu-id="83a80-109">However, the greatest taxpayers can submit declarations to the tax authority where the organization is registered as a greatest taxpayer.</span></span> <span data-ttu-id="83a80-110">В этом случае должен быть введен код **213** для атрибута **по месту**.</span><span class="sxs-lookup"><span data-stu-id="83a80-110">In this case, code **213** should be entered for the **at place of** attribute.</span></span>

<span data-ttu-id="83a80-111">Налоговая база для расчета земельного налога — кадастровая стоимость земли.</span><span class="sxs-lookup"><span data-stu-id="83a80-111">The tax base for the calculation of land tax is the cadastral cost of the land asset.</span></span> <span data-ttu-id="83a80-112">Кадастровая стоимость определяется кадастровыми органами и должна указываться пользователем на карточке основного средства.</span><span class="sxs-lookup"><span data-stu-id="83a80-112">The cadastral cost is defined by cadastral authorities and should be specified by the user on the fixed asset card.</span></span>

<span data-ttu-id="83a80-113">В этом раздел рассматривается, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="83a80-113">This topic explains how to perform the following tasks:</span></span>

1.  [<span data-ttu-id="83a80-114">Настройка земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-114">Set up land tax</span></span>](#set-up-land-tax)

2.  [<span data-ttu-id="83a80-115">Создание земельного участка и настройка параметров для расчета земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-115">Create a land asset and set up parameters for land tax calculation</span></span>](#create-a-land-asset-and-set-up-parameters-for-land-tax-calculation)

3.  [<span data-ttu-id="83a80-116">Расчет регистров земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-116">Calculate land tax registers</span></span>](#calculate-land-tax-registers)

4.  [<span data-ttu-id="83a80-117">Создание налоговой декларации по налогу на землю</span><span class="sxs-lookup"><span data-stu-id="83a80-117">Generate a land tax declaration</span></span>](#generate-a-land-tax-declaration)

5.  [<span data-ttu-id="83a80-118">Создание и разноска проводок ГК по земельному налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-118">Create and post land tax ledger transactions</span></span>](#create-and-post-land-tax-ledger-transactions)

<a name="set-up-land-tax"></a><span data-ttu-id="83a80-119">Настройка земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-119">Set up land tax</span></span>
---------------

<span data-ttu-id="83a80-120">Ниже приведен обзор шагов по настройке земельного налога:</span><span class="sxs-lookup"><span data-stu-id="83a80-120">Here is an overview of the steps for setting up land tax:</span></span>

1.  [<span data-ttu-id="83a80-121">Настройка кодов и ставок земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-121">Set up land tax codes and rates</span></span>](#set-up-land-tax-codes-and-rates)

2.  [<span data-ttu-id="83a80-122">Настройка кодов бюджетного дохода для земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-122">Set up budget revenue codes for land tax</span></span>](#set-up-budget-revenue-codes-for-land-tax)

3.  [<span data-ttu-id="83a80-123">Назначение кода бюджетного дохода налоговому коду</span><span class="sxs-lookup"><span data-stu-id="83a80-123">Assign a budget revenue code to a sales tax code</span></span>](#assign-a-budget-revenue-code-to-a-sales-tax-code)

4.  [<span data-ttu-id="83a80-124">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="83a80-124">Set up tax allowances</span></span>](#set-up-tax-allowances)

5.  [<span data-ttu-id="83a80-125">Назначение налоговых льгот налоговому коду как уменьшение ставки налога, уменьшение суммы налога и уменьшение налоговой базы</span><span class="sxs-lookup"><span data-stu-id="83a80-125">Assign tax allowances to a sales tax code as a reduction of the tax rate, a reduction of the tax amount, and a tax base reduction</span></span>](#assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-a-reduction-of-the-tax-amount-and-a-tax-base-reduction)

6.  [<span data-ttu-id="83a80-126">Настройка кода территории (кода OKTMO) для юридического лица</span><span class="sxs-lookup"><span data-stu-id="83a80-126">Set up the territory code (OKTMO code) for the legal entity</span></span>](#set-up-the-territory-code-oktmo-code-for-the-legal-entity)

7.  [<span data-ttu-id="83a80-127">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="83a80-127">Set up tax authorities and related OKTMO codes</span></span>](#set-up-tax-authorities-and-related-oktmo-codes)

8.  [<span data-ttu-id="83a80-128">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="83a80-128">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>](#optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes)

9.  [<span data-ttu-id="83a80-129">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="83a80-129">Set up the organization's locations and assign them to company divisions</span></span>](#set-up-the-organizations-locations-and-assign-them-to-company-divisions)

10. [<span data-ttu-id="83a80-130">Настройка территорий для распределенных земельных участков</span><span class="sxs-lookup"><span data-stu-id="83a80-130">Set up territories for distributed land assets</span></span>](#set-up-territories-for-distributed-land-assets)

11. [<span data-ttu-id="83a80-131">Настройка параметров ОС для разноски земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-131">Set up Fixed assets parameters for posting land tax</span></span>](#set-up-fixed-assets-parameters-for-posting-land-tax)

12. [<span data-ttu-id="83a80-132">Настройка журнала для разноски земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-132">Set up the journal for posting land tax</span></span>](#set-up-the-journal-for-posting-land-tax)

13. [<span data-ttu-id="83a80-133">Настройка групп разноски для разносок земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-133">Set up a posting group for land tax postings</span></span>](#set-up-a-posting-group-for-land-tax-postings)

### <a name="set-up-land-tax-codes-and-rates"></a><span data-ttu-id="83a80-134">Настройка кодов и ставок земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-134">Set up land tax codes and rates</span></span>

1.  <span data-ttu-id="83a80-135">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="83a80-135">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>

2.  <span data-ttu-id="83a80-136">Создайте налоговый код.</span><span class="sxs-lookup"><span data-stu-id="83a80-136">Create a sales tax code.</span></span>

3.  <span data-ttu-id="83a80-137">В поле **Тип налога** выберите **Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-137">In the **Type of tax** field, select **Land tax**.</span></span>

4.  <span data-ttu-id="83a80-138">Укажите период сопоставления и группу разноски главной книги.</span><span class="sxs-lookup"><span data-stu-id="83a80-138">Specify the settlement period and the ledger posting group.</span></span>

5.  <span data-ttu-id="83a80-139">В области действий на вкладке **Налоговый код** в группе **Налоговый код** выберите **Значения**, чтобы открыть страницу **Значения налогового кода**.</span><span class="sxs-lookup"><span data-stu-id="83a80-139">On the Action Pane, on the **Sales tax code** tab, in the **Sales tax code** group, select **Values** to open the **Sales tax code values** page.</span></span>

6.  <span data-ttu-id="83a80-140">В поле **Значение** укажите ставку налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="83a80-140">In the **Value** field, specify the tax rate for the assessed tax.</span></span>

### <a name="set-up-budget-revenue-codes-for-land-tax"></a><span data-ttu-id="83a80-141">Настройка кодов бюджетного дохода для земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-141">Set up budget revenue codes for land tax</span></span>

1.  <span data-ttu-id="83a80-142">Выберите **Управление банком и кассовыми операциями \> Настройка \> Настройка платежного поручения \> Классификация доходов бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="83a80-142">Go to **Cash and bank management \> Setup \> Payment order setup \> Budget revenue classification**.</span></span>

2.  <span data-ttu-id="83a80-143">Создайте код доходов бюджета для земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-143">Create a budget revenue code for land tax.</span></span>

### <a name="assign-a-budget-revenue-code-to-a-sales-tax-code"></a><span data-ttu-id="83a80-144">Назначение кода бюджетного дохода налоговому коду</span><span class="sxs-lookup"><span data-stu-id="83a80-144">Assign a budget revenue code to a sales tax code</span></span>

1.  <span data-ttu-id="83a80-145">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="83a80-145">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="83a80-146">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="83a80-146">Create a record.</span></span>

3.  <span data-ttu-id="83a80-147">В поле **Тип налога** выберите **Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-147">In the **Type of tax** field, select **Land tax**.</span></span>

4.  <span data-ttu-id="83a80-148">В поле **Код** выберите налоговый код земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-148">In the **Code** field, select the sales tax code for the land tax.</span></span>

5.  <span data-ttu-id="83a80-149">В поле **Код доходов бюджета** выберите Код доходов бюджета, который соответствует выбранному налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="83a80-149">In the **Budget revenue code** field, select the budget revenue code that corresponds to the selected sales tax code.</span></span>

### <a name="set-up-tax-allowances"></a><span data-ttu-id="83a80-150">Настройка налоговых льгот</span><span class="sxs-lookup"><span data-stu-id="83a80-150">Set up tax allowances</span></span>

1.  <span data-ttu-id="83a80-151">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Налоговые льготы**.</span><span class="sxs-lookup"><span data-stu-id="83a80-151">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Tax allowances**.</span></span>

2.  <span data-ttu-id="83a80-152">Создать запись.</span><span class="sxs-lookup"><span data-stu-id="83a80-152">Create a record.</span></span>

3.  <span data-ttu-id="83a80-153">Задайте следующие значения для налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="83a80-153">Set the following values for the tax allowance.</span></span>

    | <span data-ttu-id="83a80-154">Поле</span><span class="sxs-lookup"><span data-stu-id="83a80-154">Field</span></span>       | <span data-ttu-id="83a80-155">Описание</span><span class="sxs-lookup"><span data-stu-id="83a80-155">Description</span></span>                                                                                                                                                                                                                       |
    |-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="83a80-156">Привилегия</span><span class="sxs-lookup"><span data-stu-id="83a80-156">Privilege</span></span>       | <span data-ttu-id="83a80-157">Введите коды налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="83a80-157">Enter the tax allowance code.</span></span>                                                                                                                                                                                                         |
    | <span data-ttu-id="83a80-158">Тип налога</span><span class="sxs-lookup"><span data-stu-id="83a80-158">Type of tax</span></span>     | <span data-ttu-id="83a80-159">Выберите **Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-159">Select **Land tax**.</span></span>                                                                                                                                                                                                                  |
    | <span data-ttu-id="83a80-160">Тип льготы</span><span class="sxs-lookup"><span data-stu-id="83a80-160">Benefit type</span></span>    | <span data-ttu-id="83a80-161">Выберите тип налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="83a80-161">Select the type of tax allowance.</span></span> <span data-ttu-id="83a80-162">Следующие значения применяются для налоговых льгот по земельному налогу: **Освобождение от налога**, **Уменьшение налоговой базы**, **Снижение налоговой ставки**, **Уменьшение суммы налога** и **Доля необлагаемой площади**.</span><span class="sxs-lookup"><span data-stu-id="83a80-162">The following values are applicable to land tax allowances: **Exemption from tax**, **Tax base reduction**, **Reduction of tax rate**, **Reduction of tax amount**, and **Non-taxable area share**.</span></span> |
    | <span data-ttu-id="83a80-163">Название</span><span class="sxs-lookup"><span data-stu-id="83a80-163">Name</span></span>            | <span data-ttu-id="83a80-164">Введите название налоговой льготы.</span><span class="sxs-lookup"><span data-stu-id="83a80-164">Enter the name of the tax allowance.</span></span>                                                                                                                                                                                                  |
    | <span data-ttu-id="83a80-165">Величина льготы</span><span class="sxs-lookup"><span data-stu-id="83a80-165">Allowance value</span></span> | <span data-ttu-id="83a80-166">Определите значение налоговой льготы в зависимости от типа налоговой льготы, выбранного в поле **Тип льготы**:</span><span class="sxs-lookup"><span data-stu-id="83a80-166">Define the tax allowance value, depending on type of tax allowance that you selected in the **Benefit type** field:</span></span>                                                                                                                   |

    -   <span data-ttu-id="83a80-167">**Освобождение от налога:** не определяйте величину льготы, поскольку освобождение от налога всегда берется 100 процентов, а сумма налога составляет 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="83a80-167">**Exemption from tax:** Don't define the allowance value, because exemption from tax is always considered 100 percent, and the tax amount is 0 (zero).</span></span>

    -   <span data-ttu-id="83a80-168">**Уменьшение налоговой базы:** определите сумму, в местной валюте, на которую уменьшается сумма налоговой базы для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="83a80-168">**Tax base reduction:** Define the amount, in the local currency, that is reducing the tax base amount for each asset.</span></span>

    -   <span data-ttu-id="83a80-169">**Снижение налоговой ставки:** задайте процент уменьшения налоговой ставки.</span><span class="sxs-lookup"><span data-stu-id="83a80-169">**Reduction of tax rate:** Define the percentage of the tax rate reduction.</span></span>
    <span data-ttu-id="83a80-170">Например, если налоговая ставка равна 10 процентам, а налоговая льгота равна 2 процентам, уменьшенная налоговая ставка равна 8 процентам.</span><span class="sxs-lookup"><span data-stu-id="83a80-170">For example, if the tax rate is 10 percent, and the allowance value is 2 percent, the reduced tax rate is 8 percent.</span></span>

    -   <span data-ttu-id="83a80-171">**Уменьшение суммы налога:** определите сумму, в местной валюте, на которую уменьшается рассчитанная сумма налога для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="83a80-171">**Reduction of tax amount:** Define the amount, in the local currency, that is reducing the calculated tax amount for each asset.</span></span>

    -   <span data-ttu-id="83a80-172">**Доля необлагаемой площади:** значение будет определено для каждого земельного участка в записи основных средств.</span><span class="sxs-lookup"><span data-stu-id="83a80-172">**Non-taxable area share:** A value will be defined for each land asset in the fixed asset record.</span></span>

### <a name="assign-tax-allowances-to-a-sales-tax-code-as-a-reduction-of-the-tax-rate-a-reduction-of-the-tax-amount-and-a-tax-base-reduction"></a><span data-ttu-id="83a80-173">Назначение налоговых льгот налоговому коду как уменьшение ставки налога, уменьшение суммы налога и уменьшение налоговой базы</span><span class="sxs-lookup"><span data-stu-id="83a80-173">Assign tax allowances to a sales tax code as a reduction of the tax rate, a reduction of the tax amount, and a tax base reduction</span></span>

1.  <span data-ttu-id="83a80-174">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Соответствие налогов**.</span><span class="sxs-lookup"><span data-stu-id="83a80-174">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Sales tax relations**.</span></span>

2.  <span data-ttu-id="83a80-175">Выберите запись для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="83a80-175">Select the record for the sales tax code.</span></span>

3.  <span data-ttu-id="83a80-176">В полях **Льгота путем понижения ставки**, **Льгота путем уменьшения налога** и **Уменьшение налоговой базы (ч. 2 ст. 367)** выберите соответствующие налоговые льготы, если они применимы к налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="83a80-176">In the **Allowance by reduction of rate**, **Allowance by reduction of tax**, and **Tax base reduction (p.2 art.387)** fields, select the appropriate tax allowances, if they are applicable to the sales tax code.</span></span>

### <a name="set-up-the-territory-code-oktmo-code-for-the-legal-entity"></a><span data-ttu-id="83a80-177">Настройка кода территории (кода OKTMO) для юридического лица</span><span class="sxs-lookup"><span data-stu-id="83a80-177">Set up the territory code (OKTMO code) for the legal entity</span></span>

1.  <span data-ttu-id="83a80-178">Перейдите в раздел **Управление организацией \> Организации \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="83a80-178">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

2.  <span data-ttu-id="83a80-179">На экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="83a80-179">On the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

3.  <span data-ttu-id="83a80-180">На странице **Управление адресами** на экспресс-вкладке **Регистрационный номер** создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-180">On the **Manage addresses** page, on the **Registration ID** FastTab, create a line.</span></span>

4.  <span data-ttu-id="83a80-181">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="83a80-181">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    <span data-ttu-id="83a80-182">Если требуемый тип регистрации отсутствует в списке, выполните следующие действия, чтобы добавить его:</span><span class="sxs-lookup"><span data-stu-id="83a80-182">If the required registration type isn't listed, follow these steps to add it:</span></span>

    1.  <span data-ttu-id="83a80-183">На странице **Типы регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Типы регистрации**) создайте тип регистрации.</span><span class="sxs-lookup"><span data-stu-id="83a80-183">On the **Registration types** page (**Organization administration \> Global address book \> Registration types \> Registration types**), create a registration type.</span></span>

    2.  <span data-ttu-id="83a80-184">На странице **Категории регистрации** (**Управление организацией \> Глобальная адресная книга \> Типы регистрации \> Категории регистрации**) назначьте новый тип регистрации категории регистрации **ОКАТО**.</span><span class="sxs-lookup"><span data-stu-id="83a80-184">On the **Registration categories** page (**Organization administration \> Global address book \> Registration types \> Registration categories**), assign the new registration type to the **RCOAD** registration category.</span></span>

    3.  <span data-ttu-id="83a80-185">В поле **Регистрационный номер** введите код OKTMO для местоположения юридического лица.</span><span class="sxs-lookup"><span data-stu-id="83a80-185">In the **Registration number** field, enter the OKTMO code for the legal entity's location.</span></span>

### <a name="set-up-tax-authorities-and-related-oktmo-codes"></a><span data-ttu-id="83a80-186">Настройка налоговых органов и соответствующих кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="83a80-186">Set up tax authorities and related OKTMO codes</span></span>

<span data-ttu-id="83a80-187">Необходимо создать налоговые органы, в который вы должны подавать декларации по налогу на имущество.</span><span class="sxs-lookup"><span data-stu-id="83a80-187">You must create the tax authorities that you're required to report assessed tax declarations to.</span></span>

1.  <span data-ttu-id="83a80-188">Перейдите в раздел **Налог \> Косвенные налоги \> Налог \> Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="83a80-188">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax authorities**.</span></span>

2.  <span data-ttu-id="83a80-189">Создайте налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="83a80-189">Create a tax authority.</span></span>

3.  <span data-ttu-id="83a80-190">Задайте поля **Налоговый орган** и **Название**.</span><span class="sxs-lookup"><span data-stu-id="83a80-190">Set the **Authority** and **Name** fields.</span></span>

4.  <span data-ttu-id="83a80-191">В поле **Код ГНИ** введите четырехзначный код для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="83a80-191">In the **STI code** field, enter the four-digit code for the tax authority.</span></span>

5.  <span data-ttu-id="83a80-192">В поле **Счет поставщика** выберите субъект счета поставщика, который связан с налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="83a80-192">In the **Vendor account** field, select the vendor account party that is associated with the tax authority.</span></span>

6.  <span data-ttu-id="83a80-193">Определите основной код OKTMO для налогового органа для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="83a80-193">Define the main OKTMO code for the tax authority on the vendor account:</span></span>

    1.  <span data-ttu-id="83a80-194">В записи для счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="83a80-194">In the record for the vendor account, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="83a80-195">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-195">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="83a80-196">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="83a80-196">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="83a80-197">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="83a80-197">In the **Registration number** field, enter the OKTMO code.</span></span>

        > [!NOTE]
        > <span data-ttu-id="83a80-198">Для объектов недвижимости, которые расположены в главном расположении организации, налоговый орган, в который подается отчет по налогу на имущество, определяется как в налоговый орган, имеющий такой же код OKTMO, как и у юридического лица.</span><span class="sxs-lookup"><span data-stu-id="83a80-198">For realty objects that are located at the organization's main location, the tax authority that assessed tax is reported to is defined as the tax authority that has the same OKTMO code as the legal entity.</span></span>

### <a name="optional-set-up-company-divisions-their-registration-reason-codes-kpp-and-their-oktmo-codes"></a><span data-ttu-id="83a80-199">Необязательно. Настройка подразделений компании, кодов причин их регистрации (КПП) и их кодов OKTMO</span><span class="sxs-lookup"><span data-stu-id="83a80-199">Optional: Set up company divisions, their registration reason codes (KPP), and their OKTMO codes</span></span>

<span data-ttu-id="83a80-200">Если у организации имеются земельные участки, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить подразделения компании.</span><span class="sxs-lookup"><span data-stu-id="83a80-200">If the organization has land assets that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up company divisions.</span></span>

1.  <span data-ttu-id="83a80-201">Выберите **Управления организацией \> Настройка \> Обособленные подразделения**.</span><span class="sxs-lookup"><span data-stu-id="83a80-201">Go to **Organization administration \> Setup \> Separate divisions**.</span></span>

2.  <span data-ttu-id="83a80-202">Создание отдела компании.</span><span class="sxs-lookup"><span data-stu-id="83a80-202">Create a company division.</span></span>

3.  <span data-ttu-id="83a80-203">В поле **Код отдельного подразделения** введите идентификационный код для подразделения.</span><span class="sxs-lookup"><span data-stu-id="83a80-203">In the **Separate division ID** field, enter the identification code for the division.</span></span>

4.  <span data-ttu-id="83a80-204">В поле **Имя** введите имя подразделения.</span><span class="sxs-lookup"><span data-stu-id="83a80-204">In the **Name** field, enter the name of the division.</span></span>

5.  <span data-ttu-id="83a80-205">В поле **Счет поставщика** выберите номер счета поставщика, который связан с отделом.</span><span class="sxs-lookup"><span data-stu-id="83a80-205">In the **Vendor account** field, select the vendor account number that is associated with the division.</span></span> <span data-ttu-id="83a80-206">Если ни один счет поставщика недоступен для подразделения компании, необходимо создать счет.</span><span class="sxs-lookup"><span data-stu-id="83a80-206">If there is no vendor account for the company division, create one.</span></span>

6.  <span data-ttu-id="83a80-207">Определите код OKTMO для подразделения компании для счета поставщика:</span><span class="sxs-lookup"><span data-stu-id="83a80-207">Define the OKTMO code for the company division on the vendor account:</span></span>

    1.  <span data-ttu-id="83a80-208">В записи счета поставщика на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="83a80-208">In the vendor account record, on the **Addresses** FastTab, select **More options \> Advanced**.</span></span>

    2.  <span data-ttu-id="83a80-209">На экспресс-вкладке **Регистрационный номер** добавьте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-209">On the **Registration ID** FastTab, add a line.</span></span>

    3.  <span data-ttu-id="83a80-210">В поле **Тип регистрации** выберите тип регистрации для OKATO/OKTMO.</span><span class="sxs-lookup"><span data-stu-id="83a80-210">In the **Registration type** field, select the registration type for OKATO/OKTMO.</span></span>

    4.  <span data-ttu-id="83a80-211">В поле **Регистрационный номер** введите код ОКТМО.</span><span class="sxs-lookup"><span data-stu-id="83a80-211">In the **Registration number** field, enter the OKTMO code.</span></span>

7.  <span data-ttu-id="83a80-212">Повторите шаг 6, чтобы определить код КПП для обособленного подразделения для счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="83a80-212">Repeat step 6 to define the KPP code for the separate division on the vendor account.</span></span> <span data-ttu-id="83a80-213">В поле **Тип регистрации** выберите тип регистрации, с которым связана категория регистрации **КПП**.</span><span class="sxs-lookup"><span data-stu-id="83a80-213">In the **Registration type** field, select the registration type that is associated with the **KPP** registration category.</span></span>

### <a name="set-up-the-organizations-locations-and-assign-them-to-company-divisions"></a><span data-ttu-id="83a80-214">Настройка местоположений организации и назначение их подразделениям компании</span><span class="sxs-lookup"><span data-stu-id="83a80-214">Set up the organization's locations and assign them to company divisions</span></span>

<span data-ttu-id="83a80-215">Если у организации имеются земельные участки, расположенные на территориях, которые отличаются от основного местоположения организации, или если в организации имеются обособленные подразделения, следует настроить местоположения организации и назначить их подразделениям компании.</span><span class="sxs-lookup"><span data-stu-id="83a80-215">If the organization has land assets that are located in territories that differ from the organization's main location, or if the organization has separate subdivisions, you should set up organization locations and assign them to company divisions.</span></span>

1.  <span data-ttu-id="83a80-216">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="83a80-216">Go to **Fixed assets (Russia) \> Setup \> Location**.</span></span>

2.  <span data-ttu-id="83a80-217">Выберите существующее местоположение или создайте новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="83a80-217">Select an existing location, or create a new location.</span></span>

3.  <span data-ttu-id="83a80-218">На экспресс-вкладке **Общие** в поле **Код отдельного подразделения** выберите подразделение компании, созданное в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="83a80-218">On the **General** FastTab, in the **Separate division ID** field, select the company division that you created in the previous procedure.</span></span>
    
    <span data-ttu-id="83a80-219">Если поле **Код отдельного подразделения** оставлено пустым, местоположение совпадает с местоположением головного офиса организации.</span><span class="sxs-lookup"><span data-stu-id="83a80-219">If the **Separate division ID** field is left blank, the location is the same as the location of the organization's head office.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83a80-220">Для земельных участков, которые находятся на территориях, отличающихся от главного расположения организации, налоговый орган, в который подается отчет по земельному налогу, определяется как в налоговый орган с тем же кодом OKTMO, что и у обособленного подразделения, связанного с местоположением земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-220">For land assets that are located in territories that differ from the organization's main location, the tax authority that land tax is reported to is defined as the tax authority that has the same OKTMO code as the separate division that is associated with the land location.</span></span> 
    >
    > <span data-ttu-id="83a80-221">Сведения о том, как связать основное средство с местоположением, см. в разделе [Указание местоположения земельного участка](#specify-the-location-of-the-land) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="83a80-221">For information about how to associate a fixed asset with a location, see the [Specify the location of the land](#specify-the-location-of-the-land) section later in this topic.</span></span>


### <a name="set-up-territories-for-distributed-land-assets"></a><span data-ttu-id="83a80-222">Настройка территорий для распределенных земельных участков</span><span class="sxs-lookup"><span data-stu-id="83a80-222">Set up territories for distributed land assets</span></span>

<span data-ttu-id="83a80-223">Если земельный участок распределен между несколькими территориями, сведения о нем должны подаваться под соответствующим кодом OKTMO.</span><span class="sxs-lookup"><span data-stu-id="83a80-223">If a land asset is distributed among several territories, it should be reported under the appropriate OKTMO code.</span></span> <span data-ttu-id="83a80-224">Необходимо настроить территории распределения, назначить код OKTMO каждой территории и связать коды OKTMO с налоговыми органами.</span><span class="sxs-lookup"><span data-stu-id="83a80-224">You should set up distribution territories, assign an OKTMO code to each territory, and associate the OKTMO codes with tax authorities.</span></span>

1.  <span data-ttu-id="83a80-225">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Распределение**.</span><span class="sxs-lookup"><span data-stu-id="83a80-225">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Distribution**.</span></span>

2.  <span data-ttu-id="83a80-226">Создайте территорию.</span><span class="sxs-lookup"><span data-stu-id="83a80-226">Create a territory.</span></span>

3.  <span data-ttu-id="83a80-227">Задайте поля **Территория** и **Название**.</span><span class="sxs-lookup"><span data-stu-id="83a80-227">Set the **Territory** and **Name** fields.</span></span>

4.  <span data-ttu-id="83a80-228">Выберите налоговый код, который применяется к этой территории.</span><span class="sxs-lookup"><span data-stu-id="83a80-228">Select the sales tax code that is applied in the territory.</span></span>

5.  <span data-ttu-id="83a80-229">В поле **ОКАТО** выберите код ОКТМО для территории.</span><span class="sxs-lookup"><span data-stu-id="83a80-229">In the **RCOAD** field, select the OKTMO code for the territory.</span></span> <span data-ttu-id="83a80-230">Для выбора доступны только коды OKTMO, связанные с налоговым органом налогового кода.</span><span class="sxs-lookup"><span data-stu-id="83a80-230">Only OKTMO codes that are associated with the tax authority of the sales tax code are available for selection.</span></span> <span data-ttu-id="83a80-231">Если нет доступных кодов OKTMO, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83a80-231">If no OKTMO code is available, follow these steps:</span></span>

    1.  <span data-ttu-id="83a80-232">Выберите ссылку для налогового кода, чтобы открыть страницу **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="83a80-232">Select the link for the sales tax code to open the **Sales tax codes** page.</span></span>

    2.  <span data-ttu-id="83a80-233">Выберите ссылку для кода периода сопоставления налога, чтобы открыть страницу **Периоды сопоставления налогов**.</span><span class="sxs-lookup"><span data-stu-id="83a80-233">Select the link for the settlement period code to open the **Sales tax settlement periods** page.</span></span>

    3.  <span data-ttu-id="83a80-234">Выберите ссылку для кода налогового органа, чтобы открыть страницу **Налоговые органы**.</span><span class="sxs-lookup"><span data-stu-id="83a80-234">Select the link for the authority code to open the **Sales tax authorities** page.</span></span>

    4.  <span data-ttu-id="83a80-235">В области действий выберите **Коды ОКАТО**.</span><span class="sxs-lookup"><span data-stu-id="83a80-235">On the Action Pane, select **RCOAD codes**.</span></span>

    5.  <span data-ttu-id="83a80-236">Создайте строки для кодов OKTMO, которые относятся к налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="83a80-236">Create lines for the OKTMO codes that are related to the tax authority.</span></span>

> [!NOTE]
>  <span data-ttu-id="83a80-237">Можно также создать все коды OKTMO и затем присвоить код налоговому органу на странице **Коды ОКАТО** (**Налог \> Настройка \> Налог с продаж \> Коды ОКАТО**).</span><span class="sxs-lookup"><span data-stu-id="83a80-237">Alternatively, create all the OKTMO codes, and then assign a code to the tax authority on the **RCOAD codes** page (**Tax \> Setup \> Sales tax \> RCOAD codes**).</span></span>

### <a name="set-up-fixed-assets-parameters-for-posting-land-tax"></a><span data-ttu-id="83a80-238">Настройка параметров ОС для разноски земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-238">Set up Fixed assets parameters for posting land tax</span></span>

1.  <span data-ttu-id="83a80-239">Перейдите в раздел **Основные средства (Россия) \> Настройка \> Параметры**.</span><span class="sxs-lookup"><span data-stu-id="83a80-239">Go to **Fixed assets (Russia) \> Setup \> Parameters**.</span></span>

2.  <span data-ttu-id="83a80-240">На вкладке **Номерные серии** для ссылки **Номер журнала регистров налога на имущество** выберите номерную серию для налогового регистра.</span><span class="sxs-lookup"><span data-stu-id="83a80-240">On the **Number sequences** tab, for the **Assessed tax registers journal number** reference, select a number sequence for the tax register.</span></span>

3.  <span data-ttu-id="83a80-241">На вкладке **Налоговая отчетность** в разделе **Земельный налог** в поле **Код налога** выберите код налога по умолчанию для земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-241">On the **Tax reporting** tab, in the **Land tax** section, in the **Sales tax code** field, select the default sales tax code for land tax.</span></span>

4.  <span data-ttu-id="83a80-242">В поле **Сжатие** выберите уровень сжатия для проводок земельного налога:</span><span class="sxs-lookup"><span data-stu-id="83a80-242">In the **Compression** field, select the level of compression for land tax transactions:</span></span>

    -  <span data-ttu-id="83a80-243">**Налог** — подробный журнал книги учета для проводок по земельному налогу будет создаваться для каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="83a80-243">**Tax** – A detailed ledger journal for land tax transactions will be created for each sales tax code.</span></span>

    -  <span data-ttu-id="83a80-244">**Итог** — журнал книги учета для проводок земельного налога будет создаваться как одна строка с кодом налога по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83a80-244">**Total** – A ledger journal for land tax transactions will be created as one line that has the default sales tax code.</span></span>

5.  <span data-ttu-id="83a80-245">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83a80-245">Close the page.</span></span>

### <a name="set-up-the-journal-for-posting-land-tax"></a><span data-ttu-id="83a80-246">Настройка журнала для разноски земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-246">Set up the journal for posting land tax</span></span>

<span data-ttu-id="83a80-247">Если проводки по земельному налогу будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить журнал.</span><span class="sxs-lookup"><span data-stu-id="83a80-247">If land tax transactions will be automatically created based on calculated tax registers, you should set up a journal.</span></span>

1.  <span data-ttu-id="83a80-248">Перейдите в раздел **Главная книга \> Настройка журнала \> Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="83a80-248">Go to **General ledger \> Journal setup \> Journal names**.</span></span>

2.  <span data-ttu-id="83a80-249">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-249">Create a line.</span></span>

3.  <span data-ttu-id="83a80-250">Задайте поля **Название** и **Серии ваучеров**.</span><span class="sxs-lookup"><span data-stu-id="83a80-250">Set the **Name** and **Voucher series** fields.</span></span>

4.  <span data-ttu-id="83a80-251">В поле **Тип журнала** выберите **Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-251">In the **Journal type** field, select **Land tax**.</span></span>

### <a name="set-up-a-posting-group-for-land-tax-postings"></a><span data-ttu-id="83a80-252">Настройка групп разноски для разносок земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-252">Set up a posting group for land tax postings</span></span>

<span data-ttu-id="83a80-253">Если проводки по земельному налогу будут автоматически создаваться на основе рассчитанных регистров налога, следует настроить группы разноски.</span><span class="sxs-lookup"><span data-stu-id="83a80-253">If land tax transactions will be automatically created based on calculated tax registers, you should set up posting groups.</span></span>

1.  <span data-ttu-id="83a80-254">Выберите **Основные средства (Россия) \> Настройка \> Налоговая отчетность \> Группа разноски по налогам**.</span><span class="sxs-lookup"><span data-stu-id="83a80-254">Go to **Fixed assets (Russia) \> Setup \> Tax reporting \> Group of posting of taxes**.</span></span>

2.  <span data-ttu-id="83a80-255">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-255">Create a line.</span></span>

3.  <span data-ttu-id="83a80-256">В поле **Группа разноски ГК** выберите группу разноски ГК для земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-256">In the **Ledger posting group** field, select a ledger posting group for land tax.</span></span>

    <span data-ttu-id="83a80-257">Если в списке нет ни одной группы разноски ГК, создайте ее.</span><span class="sxs-lookup"><span data-stu-id="83a80-257">If no ledger posting group is listed, create one.</span></span> <span data-ttu-id="83a80-258">В поле **Исходящий налог** введите номер счета ГК для разноски земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-258">In the **Sales tax payable** field, enter the ledger account code for posting land tax.</span></span>

1.  <span data-ttu-id="83a80-259">В поле **Счет для налогов ОС** выберите счет ГК для расходов по земельному налогу.</span><span class="sxs-lookup"><span data-stu-id="83a80-259">In the **Account for FA taxes** field, select a ledger account for the land tax expenses.</span></span>

2.  <span data-ttu-id="83a80-260">Убедитесь, что в поле **Исходящий налог** установлено значение кода счета ГК, введенного для группы разноски главной книги на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="83a80-260">Make sure that the **Sales tax payable** field is set to the ledger account code that you entered for the ledger posting group in step 3.</span></span>

<a name="create-a-land-asset-and-set-up-parameters-for-land-tax-calculation"></a><span data-ttu-id="83a80-261">Создание земельного участка и настройка параметров для расчета земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-261">Create a land asset and set up parameters for land tax calculation</span></span>
------------------------------------------------------------------

<span data-ttu-id="83a80-262">Ниже приведен обзор шагов для создания земельного участка и настройки параметров для расчета земельного налога:</span><span class="sxs-lookup"><span data-stu-id="83a80-262">Here is an overview of the steps for creating a land asset and setting up parameters for land tax calculation:</span></span>

1.  <span data-ttu-id="83a80-263">Создание земельного участка и определение параметров для расчета земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-263">Create a land fixed asset and define parameters for land tax calculation</span></span>

2.  [<span data-ttu-id="83a80-264">Указание местоположения земельного участка</span><span class="sxs-lookup"><span data-stu-id="83a80-264">Specify the location of the land</span></span>](#specify-the-location-of-the-land)

3.  [<span data-ttu-id="83a80-265">Указание распределения для земельного участка, расположенного на нескольких территориях</span><span class="sxs-lookup"><span data-stu-id="83a80-265">Specify the distribution for a land asset that is located in several territories</span></span>](#specify-the-distribution-for-a-land-asset-that-is-located-in-several-territories)

4.  [<span data-ttu-id="83a80-266">Изменение кадастровой стоимости земли и указание журнала льгот по налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-266">Change the cadastral cost of land and specify the tax allowance history</span></span>](#change-the-cadastral-cost-of-land-and-specify-the-tax-allowance-history)

5.  [<span data-ttu-id="83a80-267">Изменение кадастровой стоимости распределенного земельного участка</span><span class="sxs-lookup"><span data-stu-id="83a80-267">Change the cadastral cost of a distributed land asset</span></span>](#change-the-cadastral-cost-of-a-distributed-land-asset)

### <a name="create-a-land-fixed-asset-and-define-parameters-for-land-tax-calculation"></a><span data-ttu-id="83a80-268">Создание земельного участка и определение параметров для расчета земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-268">Create a land fixed asset and define parameters for land tax calculation</span></span>

1.  <span data-ttu-id="83a80-269">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="83a80-269">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="83a80-270">Выберите существующее основное средство или создайте новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="83a80-270">Select an existing fixed asset, or create a new fixed asset.</span></span>

3.  <span data-ttu-id="83a80-271">На экспресс-вкладке **Общее** в поле **Тип** выберите **Земельный участок**.</span><span class="sxs-lookup"><span data-stu-id="83a80-271">On the **General** FastTab, in the **Type** field, select **Ground area**.</span></span>

4.  <span data-ttu-id="83a80-272">В поле **Флаг владения** выберите, находится ли основное средство в собственности, операционном управлении, аренде или владении лица за пределами России.</span><span class="sxs-lookup"><span data-stu-id="83a80-272">In the **Flag of ownership** field, select whether the fixed asset is owned, under operational management, leased, or owned by someone who is outside Russia.</span></span>

5.  <span data-ttu-id="83a80-273">На экспресс-вкладке **Техническая информация** задайте поля **Категория** и **Кадастровый номер** для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-273">On the **Technical information** FastTab, set the **Category** and **Cadastral number** fields for the land asset.</span></span>

6.  <span data-ttu-id="83a80-274">Задайте поле **Дата начала строительства**, если земельный участок был приобретен для строительства.</span><span class="sxs-lookup"><span data-stu-id="83a80-274">Set the **Start date of building** field if the land was acquired for housing construction.</span></span> <span data-ttu-id="83a80-275">Специальные коэффициенты, которые зависят от периода строительства, будут применяться к земельным участкам этого типа, когда рассчитывается земельный налог.</span><span class="sxs-lookup"><span data-stu-id="83a80-275">Special coefficients that depend on the building period will be applied to land assets of this type when land tax is calculated.</span></span> <span data-ttu-id="83a80-276">Если период строительства превысил три года в течение налогового периода, декларация по земельному налогу будут содержать два вхождения раздела 3: один экземпляр для земельного налога до истечения трех лет и второй экземпляр для земельного налога после трех лет.</span><span class="sxs-lookup"><span data-stu-id="83a80-276">If the construction period exceeded three years during the tax period, the land tax declaration will include two occurrences of Section 3: one occurrence for land tax before three years passed and one occurrence for land tax after three years passed.</span></span>

7.  <span data-ttu-id="83a80-277">На экспресс-вкладке **Налоговая отчетность** в разделе **Земельный налог** в поле **Налоговая база** введите кадастровую стоимость земли.</span><span class="sxs-lookup"><span data-stu-id="83a80-277">On the **Tax reporting** FastTab, in the **Land tax** section, in the **Tax base** field, enter the cadastral cost of the land.</span></span>

8.  <span data-ttu-id="83a80-278">В поле **Налоговый код** выберите налоговый код для расчета налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="83a80-278">In the **Sales tax code** field, select the sales tax code for the assessed tax calculation.</span></span>

9.  <span data-ttu-id="83a80-279">Если вы частично владеете основным средством, в полях **Числитель доли собственности** и **Знаменатель доли собственности** определите свою долю собственности в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="83a80-279">If you partially own the fixed asset, in the **Owned share numerator** and **Owned share denominator** fields, define your ownership share as a simple fraction.</span></span>

### <a name="specify-the-location-of-the-land"></a><span data-ttu-id="83a80-280">Указание местоположения земельного участка</span><span class="sxs-lookup"><span data-stu-id="83a80-280">Specify the location of the land</span></span>

<span data-ttu-id="83a80-281">По умолчанию предполагается, что земельные участки расположены в месте расположения организации и отчет о них направляется налоговым органам на территории юридического лица.</span><span class="sxs-lookup"><span data-stu-id="83a80-281">By default, the assumption is that land assets are located at the organization's location and reported to the tax authority in the legal entity's territory.</span></span> <span data-ttu-id="83a80-282">(Код налогового органа OKTMO соответствует коду OKTMO юридического лица, и земельные участки включаются в отчет под тем же кодом OKTMO.)</span><span class="sxs-lookup"><span data-stu-id="83a80-282">(The OKTMO code of the tax authority matches the OKTMO code of the legal entity, and land assets are reported under the same OKTMO code.)</span></span>

<span data-ttu-id="83a80-283">Если у организации есть земельные участки, которые находятся на других территориях и зарегистрированы в других налоговых органах, необходимо указать местоположение земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-283">If the organization has land assets that are located in different territories and registered in different tax authorities, you must specify the location of the land asset.</span></span>

1.  <span data-ttu-id="83a80-284">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="83a80-284">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="83a80-285">Выберите строку для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-285">Select the line for the land asset.</span></span>

3.  <span data-ttu-id="83a80-286">В области действий на вкладке **Основные средства** в группе **История** выберите **Передача**.</span><span class="sxs-lookup"><span data-stu-id="83a80-286">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Transfer**.</span></span>

4.  <span data-ttu-id="83a80-287">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-287">Create a line.</span></span>

5.  <span data-ttu-id="83a80-288">Задайте поля **Дата** и **Новое местоположение**.</span><span class="sxs-lookup"><span data-stu-id="83a80-288">Set the **Date** and **New location** fields.</span></span>

### <a name="specify-the-distribution-for-a-land-asset-that-is-located-in-several-territories"></a><span data-ttu-id="83a80-289">Указание распределения для земельного участка, расположенного на нескольких территориях</span><span class="sxs-lookup"><span data-stu-id="83a80-289">Specify the distribution for a land asset that is located in several territories</span></span>

1.  <span data-ttu-id="83a80-290">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="83a80-290">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="83a80-291">Выберите строку для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-291">Select the line for the land asset.</span></span>

3.  <span data-ttu-id="83a80-292">В области действий на вкладке **Основные средства** в группе **Распределение** выберите **Распределение**.</span><span class="sxs-lookup"><span data-stu-id="83a80-292">On the Action Pane, on the **Fixed asset** tab, in the **Distribution** group, select **Distribution**.</span></span>

4.  <span data-ttu-id="83a80-293">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-293">Create a line.</span></span>

5.  <span data-ttu-id="83a80-294">В поле **Местоположение** выберите территорию.</span><span class="sxs-lookup"><span data-stu-id="83a80-294">In the **Location** field, select a territory.</span></span>

6.  <span data-ttu-id="83a80-295">Проверьте значения в полях **ОКАТО** и **Код налога**.</span><span class="sxs-lookup"><span data-stu-id="83a80-295">Review the values in the **RCOAD** and **Sales tax code** fields.</span></span> <span data-ttu-id="83a80-296">Эти значения автоматически вводятся из записи расположения территории.</span><span class="sxs-lookup"><span data-stu-id="83a80-296">These values are automatically entered from the territory location record.</span></span>

7.  <span data-ttu-id="83a80-297">В поле **Налоговая база** укажите кадастровую стоимость земли на заданной территории.</span><span class="sxs-lookup"><span data-stu-id="83a80-297">In the **Tax base** field, specify the cadastral cost of the land in the specified territory.</span></span>

8.  <span data-ttu-id="83a80-298">Если вы частично владеете основным средством, в полях **Числитель доли собственности** и **Знаменатель доли собственности** определите свою долю собственности в указанной территории в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="83a80-298">If you partially own the fixed asset, in the **Owned share numerator** and **Owned share denominator** fields, define your ownership share in the specified territory as a simple fraction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83a80-299">При создании строки для изменения кадастровой стоимости поля **Налоговая** база и **Налог** в записи ОС больше нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="83a80-299">When the line for the change in cadastral value is created, the **Tax base** and **Sales tax** fields in the fixed asset record can no longer be edited.</span></span>

### <a name="change-the-cadastral-cost-of-land-and-specify-the-tax-allowance-history"></a><span data-ttu-id="83a80-300">Изменение кадастровой стоимости земли и указание журнала льгот по налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-300">Change the cadastral cost of land and specify the tax allowance history</span></span>

<span data-ttu-id="83a80-301">Кадастровая стоимость земельного участка может измениться вследствие изменения качественных и количественных характеристик.</span><span class="sxs-lookup"><span data-stu-id="83a80-301">The cadastral cost of a land asset might change because of a change in qualitative and quantitative characteristics.</span></span> <span data-ttu-id="83a80-302">Выполните следующие действия, чтобы записать изменения в кадастровой стоимости.</span><span class="sxs-lookup"><span data-stu-id="83a80-302">Follow these steps to record a change in cadastral value.</span></span>

1.  <span data-ttu-id="83a80-303">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="83a80-303">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="83a80-304">Выберите строку для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-304">Select the line for the land asset.</span></span>

3.  <span data-ttu-id="83a80-305">В области действий на вкладке **Основные средства** в группе **История** выберите **Данные налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="83a80-305">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Tax reporting data**.</span></span>

4.  <span data-ttu-id="83a80-306">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-306">Create a line.</span></span>

5.  <span data-ttu-id="83a80-307">В поле **Период** укажите месяц, когда изменилась кадастровая стоимость.</span><span class="sxs-lookup"><span data-stu-id="83a80-307">In the **Period** field, specify the month when the cadastral value is changing.</span></span>

6.  <span data-ttu-id="83a80-308">В поле **Налоговая база** укажите новую кадастровую стоимость земли.</span><span class="sxs-lookup"><span data-stu-id="83a80-308">In the **Tax base** field, specify the new cadastral value of the land.</span></span> <span data-ttu-id="83a80-309">Кроме того, необходимо указать любые другие измененные значения: **Категория**, **Кадастровый номер**, **Числитель доли собственности** или **Знаменатель доли собственности**.</span><span class="sxs-lookup"><span data-stu-id="83a80-309">Also specify any other values that have changed: **Category**, **Cadastral number**, **Owned share numerator**, or **Owned share denominator**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83a80-310">Если это изменение будет первым изменением кадастровой стоимости, необходимо также создать строку для предыдущего значения, которое изначально было введено в запись основного средства.</span><span class="sxs-lookup"><span data-stu-id="83a80-310">If this change is the first change in cadastral value, you must also create a line for the previous values that were originally entered in the fixed asset record.</span></span>
    >  
    > <span data-ttu-id="83a80-311">При создании строки для изменения кадастровой стоимости соответствующие поля в записи ОС больше нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="83a80-311">When the line for the change in cadastral value is created, corresponding fields in the fixed asset record can no longer be edited.</span></span> <span data-ttu-id="83a80-312">Они отображают фактические значения из записи журнала данных налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="83a80-312">They show the actual values from the tax reporting data history record.</span></span>
    >  
    > <span data-ttu-id="83a80-313">Страница **Журнал данных налоговой отчетности** используется для определения истории изменений налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="83a80-313">Use the **History of tax reporting data** page to define the history of tax allowance changes.</span></span>

7.  <span data-ttu-id="83a80-314">В поле **Освобождение от налога на землю (ст. 387)** укажите код налоговой льготы как освобождение от налога в соответствии с федеральным законодательством.</span><span class="sxs-lookup"><span data-stu-id="83a80-314">In the **Land tax exemption (art 387)** field, specify the code for the tax allowance as an exemption from tax in accordance with federal law.</span></span>
    <span data-ttu-id="83a80-315">Можно также в поле **Освобождение от налога на землю (ст. 395)** указать код налоговой льготы как освобождение от налога в соответствии с региональным законодательством.</span><span class="sxs-lookup"><span data-stu-id="83a80-315">Alternatively, in the **Land tax exemption (art 395)** field, specify the code for the tax allowance as an exemption from tax in accordance with regional law.</span></span>

8.  <span data-ttu-id="83a80-316">Задайте поле **Налоговая льгота как необлагаемая налогом доля**, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="83a80-316">Set the **Land tax allowance as non-taxable share** field, if it's applicable.</span></span>

    <span data-ttu-id="83a80-317">При добавлении значений налоговых льгот соответствующие поля в записи ОС показывают фактические значения из записи журнала данных налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="83a80-317">When the values for tax allowances are added, corresponding fields in the fixed asset record show the actual values from the tax reporting data history record.</span></span>

### <a name="change-the-cadastral-cost-of-a-distributed-land-asset"></a><span data-ttu-id="83a80-318">Изменение кадастровой стоимости распределенного земельного участка</span><span class="sxs-lookup"><span data-stu-id="83a80-318">Change the cadastral cost of a distributed land asset</span></span>

<span data-ttu-id="83a80-319">Если кадастровая стоимость земельного участка, расположенного на нескольких территориях, изменяется, выполните следующие шаги, чтобы указать новую кадастровую стоимость для каждой территории.</span><span class="sxs-lookup"><span data-stu-id="83a80-319">If the cadastral cost of a land asset that is located in several territories changes, follow these steps to specify the new cadastral cost in each territory.</span></span>

1.  <span data-ttu-id="83a80-320">Перейдите в раздел **Основные средства (Россия) \> Общие \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="83a80-320">Go to **Fixed assets (Russia) \> Common \> Fixed assets**.</span></span>

2.  <span data-ttu-id="83a80-321">Выберите строку для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-321">Select the line for the land asset.</span></span>

3.  <span data-ttu-id="83a80-322">В области действий на вкладке **Основные средства** в группе **Распределение** выберите **Распределение**.</span><span class="sxs-lookup"><span data-stu-id="83a80-322">On the Action Pane, on the **Fixed asset** tab, in the **Distribution** group, select **Distribution**.</span></span>

4.  <span data-ttu-id="83a80-323">Выберите строку для распределения, затем на панели операций выберите **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="83a80-323">Select the line for the distribution, and then, on the Action Pane, select **History**.</span></span>

5.  <span data-ttu-id="83a80-324">Создайте строку.</span><span class="sxs-lookup"><span data-stu-id="83a80-324">Create a line.</span></span>

6.  <span data-ttu-id="83a80-325">В поле **Период** укажите месяц, когда изменилась кадастровая стоимость.</span><span class="sxs-lookup"><span data-stu-id="83a80-325">In the **Period** field, specify the month when the cadastral value is changing.</span></span>

7.  <span data-ttu-id="83a80-326">В поле **Налоговая база** укажите новую кадастровую стоимость земли.</span><span class="sxs-lookup"><span data-stu-id="83a80-326">In the **Tax base** field, specify the new cadastral value of the land.</span></span> <span data-ttu-id="83a80-327">Кроме того, необходимо указать любые другие измененные значения: **Числитель доли собственности** или **Знаменатель доли собственности**.</span><span class="sxs-lookup"><span data-stu-id="83a80-327">Also specify any other values that have changed: **Owned share numerator** or **Owned share denominator**.</span></span>

> [!NOTE] 
> <span data-ttu-id="83a80-328">Если это изменение будет первым изменением кадастровой стоимости, необходимо также создать строку для предыдущего значения, которое изначально было введено в запись распределения.</span><span class="sxs-lookup"><span data-stu-id="83a80-328">If this change is the first change in cadastral value, you must also create a line for the previous values that were originally entered in the distribution record.</span></span>
>
> <span data-ttu-id="83a80-329">При создании строки для изменения кадастровой стоимости соответствующие поля в записи распределения больше нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="83a80-329">When the line for the change in cadastral value is created, corresponding fields in the distribution record can no longer be edited.</span></span> <span data-ttu-id="83a80-330">Они отображают фактические значения из записи журнала.</span><span class="sxs-lookup"><span data-stu-id="83a80-330">They show the actual values from the history record.</span></span>

<a name="calculate-land-tax-registers"></a><span data-ttu-id="83a80-331">Расчет регистров земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-331">Calculate land tax registers</span></span>
----------------------------

<span data-ttu-id="83a80-332">После завершения настройки, регистрации приобретения земельных участков и настройки всех параметров земельных участков для расчета земельного налога, необходимо рассчитать регистры налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="83a80-332">After you've finished the setup, registered the acquisition of land assets, and set up all land asset parameters for land tax calculation, you must calculate land tax registers.</span></span> <span data-ttu-id="83a80-333">Доступны следующие налоговые регистры:</span><span class="sxs-lookup"><span data-stu-id="83a80-333">The following tax registers are available:</span></span>

-   <span data-ttu-id="83a80-334">**Земельный налог — земельные участки** — этот налоговый регистр рассчитывает земельный налог для каждого земельного участка.</span><span class="sxs-lookup"><span data-stu-id="83a80-334">**Land tax – ground areas** – This tax register calculates land tax for each land asset.</span></span> <span data-ttu-id="83a80-335">Для всех земельных участков, расположенных в территории, указанной кодом ОКТМО, в регистре отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="83a80-335">For each land asset that is located in a territory that is specified by an OKTMO code, the register shows the following information:</span></span>

    -   <span data-ttu-id="83a80-336">Категория земельного участка и кадастровый номер.</span><span class="sxs-lookup"><span data-stu-id="83a80-336">The land category and cadastral number.</span></span>

-   <span data-ttu-id="83a80-337">**Период проектирования и строительства** — возможны значения **3 года** и **Более 3 лет**.</span><span class="sxs-lookup"><span data-stu-id="83a80-337">**Design and building period** – The possible values are **3 years** and     **More than 3 years**.</span></span>

    -   <span data-ttu-id="83a80-338">Кадастровая стоимость и доля собственности в виде простой дроби.</span><span class="sxs-lookup"><span data-stu-id="83a80-338">The cadastral cost, and the owned share as a simple fraction.</span></span>

    -   <span data-ttu-id="83a80-339">Коды и суммы налоговых льгот.</span><span class="sxs-lookup"><span data-stu-id="83a80-339">Tax allowance codes and amounts.</span></span>

    -   <span data-ttu-id="83a80-340">База налога на указанном территории и налоговая ставка.</span><span class="sxs-lookup"><span data-stu-id="83a80-340">The tax base in the specified territory and the tax rate.</span></span>

    -   <span data-ttu-id="83a80-341">Период владения и коэффициент, если земля была приобретена или продана в течение этого периода, либо если период строительства превысил три года за этот период.</span><span class="sxs-lookup"><span data-stu-id="83a80-341">The ownership period and factor, if the land was acquired or sold during the period, or if the housing building period exceeded three years during the period.</span></span>

    -   <span data-ttu-id="83a80-342">Период и коэффициент изменения стоимости, если кадастровая стоимость изменилась в течение периода.</span><span class="sxs-lookup"><span data-stu-id="83a80-342">The cost change period and factor, if the cadastral cost changed during the period.</span></span>

-   <span data-ttu-id="83a80-343">**Рассчитанный авансовый платеж/налог** — если налоговый регистр рассчитывается для первого квартала, второго квартала или третьего квартала, сумма налогового аванса до применения налоговых вычетов как уменьшение налоговой ставки или уменьшение суммы налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-343">**Calculated advance payment/Tax** – If the tax register is calculated for the first quarter, second quarter, or third quarter, the tax advance amount before tax allowances are applied as a reduction of the tax rate or a reduction of tax amount.</span></span> <span data-ttu-id="83a80-344">Если налоговый регистр рассчитывается для года, сумма земельного налога до применения налоговых льгот будет применяться как уменьшение налоговой ставки или уменьшения суммы налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-344">If the tax register is calculated for the year, the land tax amount before tax allowances are applied as a reduction of the tax rate or a reduction of the tax amount.</span></span>

-   <span data-ttu-id="83a80-345">**Сумма авансового платежа/Сумма налога** — если налоговый регистр рассчитывается для первого квартала, второго квартала или третьего квартала, окончательная сумма налогового аванса.</span><span class="sxs-lookup"><span data-stu-id="83a80-345">**Advance payment amount/Tax amount** – If the tax register is calculated for the first quarter, second quarter, or third quarter, the final tax advance amount.</span></span> <span data-ttu-id="83a80-346">Если налоговый регистр рассчитывается за год, то окончательная сумма земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-346">If the tax register is calculated for the year, the final land tax amount.</span></span>

-   <span data-ttu-id="83a80-347">**Земельный налог** — этот налоговый регистр рассчитывает итоговые суммы земельного налога для каждого налогового кода и кода OKTMO.</span><span class="sxs-lookup"><span data-stu-id="83a80-347">**Land tax** – This tax register calculates total land tax amounts for each sales tax code and OKTMO code.</span></span>

<span data-ttu-id="83a80-348">Чтобы рассчитать и утвердить регистры земельного налога, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83a80-348">To calculate and approve land tax registers, follow these steps.</span></span>

1.  <span data-ttu-id="83a80-349">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="83a80-349">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="83a80-350">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="83a80-350">Select **New**.</span></span>

3.  <span data-ttu-id="83a80-351">В поле **Тип налога** выберите **Земельный налог** для создания журнала только для регистров земельного налога или оставьте это поле пустым, чтобы создать журнал для всех налогов на ОС (налога на имущество, земельного налога и транспортного налога).</span><span class="sxs-lookup"><span data-stu-id="83a80-351">In the **Type of tax** field, either select **Land tax** to create a journal only for land tax registers, or leave the field blank to create a journal for all the asset's taxes (assessed tax, land tax, and transport tax).</span></span>

4.  <span data-ttu-id="83a80-352">В поле **Типы периодов** выберите один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="83a80-352">In the **Period types** field, select one of the following values:</span></span>

    -   <span data-ttu-id="83a80-353">**Квартал** — создание журнала для расчета авансовых платежей по земельному налогу.</span><span class="sxs-lookup"><span data-stu-id="83a80-353">**Quarter** – Generate a journal for the calculation of land tax advance payments.</span></span>

    -   <span data-ttu-id="83a80-354">**Годы** — создание журнала для расчета годового земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-354">**Years** – Generate a journal for the annual land tax calculation.</span></span>

5.  <span data-ttu-id="83a80-355">В поле **Номер периода**, если вы установили **Квартал** в поле **Типы периодов**, введите номер квартала.</span><span class="sxs-lookup"><span data-stu-id="83a80-355">In the **Period number** field, if you selected **Quarter** in the **Period types** field, enter the number of the quarter.</span></span> <span data-ttu-id="83a80-356">Если вы выбрали **Годы**, введите **1**.</span><span class="sxs-lookup"><span data-stu-id="83a80-356">If you selected **Years**, enter **1**.</span></span>

6.  <span data-ttu-id="83a80-357">В полях **Годы** введите отчетный год в формате *ГГГГ*.</span><span class="sxs-lookup"><span data-stu-id="83a80-357">In the **Years** fields, enter the reporting year in *YYYY* format.</span></span>

7.  <span data-ttu-id="83a80-358">Выберите **ОК**, чтобы создать журнал.</span><span class="sxs-lookup"><span data-stu-id="83a80-358">Select **OK** to create the journal.</span></span>

8.  <span data-ttu-id="83a80-359">Выберите **Строки**, чтобы создать строки в периодическом журнала регистров.</span><span class="sxs-lookup"><span data-stu-id="83a80-359">Select **Lines** to create lines in the periodic register journal.</span></span>

9.  <span data-ttu-id="83a80-360">Вы получаете сообщение о том, что "Журнал регистров не создавался.</span><span class="sxs-lookup"><span data-stu-id="83a80-360">You receive a message that states, "Register journal has not been created yet.</span></span> <span data-ttu-id="83a80-361">Создать журнал?"</span><span class="sxs-lookup"><span data-stu-id="83a80-361">Do you want create it?"</span></span> <span data-ttu-id="83a80-362">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="83a80-362">Select **Yes**.</span></span>

10. <span data-ttu-id="83a80-363">Проверьте налоговые регистры, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="83a80-363">Review the tax registers that are created.</span></span> <span data-ttu-id="83a80-364">Для земельного налога создаются следующие регистры: **Земельный налог — земельные участки** и **Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-364">For land tax, the following registers are created: **Land tax – ground areas** and **Land tax**.</span></span>

11. <span data-ttu-id="83a80-365">Чтобы рассчитать конкретный налоговый регистр в журнале, выберите этот регистр, затем выберите **Рассчитать текущий**.</span><span class="sxs-lookup"><span data-stu-id="83a80-365">To calculate a specific tax register in the journal, select the register, and then select **Calculate current**.</span></span> <span data-ttu-id="83a80-366">Чтобы рассчитать все налоговые регистры в журнале, выберите **Рассчитать все**.</span><span class="sxs-lookup"><span data-stu-id="83a80-366">To calculate all tax registers in the journal, select **Calculate all**.</span></span>

12. <span data-ttu-id="83a80-367">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83a80-367">Select **OK**.</span></span>

13. <span data-ttu-id="83a80-368">Выберите налоговый регистр, затем выберите **Строки регистра** для просмотра рассчитанных строк.</span><span class="sxs-lookup"><span data-stu-id="83a80-368">Select a tax register, and then select **Register lines** to review the calculated lines.</span></span>

14. <span data-ttu-id="83a80-369">Выберите **Печать** для печати строк налогового регистра в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="83a80-369">Select **Print** to print the tax register lines in Microsoft Excel.</span></span>

15. <span data-ttu-id="83a80-370">Выберите **Сброс статуса**, чтобы сбросить статус рассчитанного регистра на **Не рассчитано**.</span><span class="sxs-lookup"><span data-stu-id="83a80-370">Select **Reset status** to reset the status of the calculated register to **Not calculated**.</span></span>

16. <span data-ttu-id="83a80-371">Когда закончите просмотр данных в налоговых регистрах, выберите флажок **Утверждено**, чтобы утвердить каждой регистр.</span><span class="sxs-lookup"><span data-stu-id="83a80-371">After you've finished reviewing the data in the tax registers, select the **Approved** check box to approve each register.</span></span>

17. <span data-ttu-id="83a80-372">В поле **Рабочий** просмотрите или измените код для утвердившего регистр сотрудника.</span><span class="sxs-lookup"><span data-stu-id="83a80-372">In the **Worker** field, view or change the code for the employee who approved the register.</span></span>

### <a name="create-and-calculate-corrective-tax-registers"></a><span data-ttu-id="83a80-373">Создание и расчет корректирующих налоговых регистров</span><span class="sxs-lookup"><span data-stu-id="83a80-373">Create and calculate corrective tax registers</span></span>

<span data-ttu-id="83a80-374">Если вы корректировали какие-либо данные земельного участка за предыдущие периоды, следует создать корректирующие налоговые регистры, чтобы отразить исправленные суммы земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-374">If you've corrected any land asset data for the previous periods, you should create corrective tax registers to reflect the corrected land tax amounts.</span></span>

<span data-ttu-id="83a80-375">Чтобы создать корректирующие регистры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83a80-375">To create corrective registers, follow these steps.</span></span>

1.  <span data-ttu-id="83a80-376">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="83a80-376">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="83a80-377">Выберите утвержденный журнал для периода, который необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="83a80-377">Select the approved journal for the period that must be corrected.</span></span>

3.  <span data-ttu-id="83a80-378">Выберите **Коррекция \> Исправления в текущем журнале**.</span><span class="sxs-lookup"><span data-stu-id="83a80-378">Select **Correction \> Corrections to current journal**.</span></span>

4.  <span data-ttu-id="83a80-379">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="83a80-379">Select **New**.</span></span>

5.  <span data-ttu-id="83a80-380">В поле **Тип налога** выберите **Земельный налог**, если необходимо исправить только регистры земельного налога, или оставить это поле пустым, если необходимо исправить все налоговые регистры актива.</span><span class="sxs-lookup"><span data-stu-id="83a80-380">In the **Type of tax** field, either select **Land tax** if you must correct only land tax registers, or leave the field blank if you must correct all the asset's tax registers.</span></span>

6.  <span data-ttu-id="83a80-381">Убедитесь, что в полях **Типы периодов**, **Номер периода** и **Годы** заданы значения, которые подходят для периода регистра, который нужно исправить.</span><span class="sxs-lookup"><span data-stu-id="83a80-381">Make sure that the **Period types**, **Period number**, and **Years** fields are set to values that are appropriate for the period of the register that you're correcting.</span></span>

7.  <span data-ttu-id="83a80-382">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83a80-382">Select **OK**.</span></span>

8.  <span data-ttu-id="83a80-383">Создайте строки налогового регистра и рассчитайте и утвердите налоговые регистры, как описано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="83a80-383">Create tax register lines, and calculate and approve the tax registers as described in the previous procedure.</span></span>

<a name="generate-a-land-tax-declaration"></a><span data-ttu-id="83a80-384">Создание налоговой декларации по налогу на землю</span><span class="sxs-lookup"><span data-stu-id="83a80-384">Generate a land tax declaration</span></span>
-------------------------------

### <a name="set-up-the-system-to-generate-a-land-tax-declaration"></a><span data-ttu-id="83a80-385">Настройка системы для создания декларации по земельного налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-385">Set up the system to generate a land tax declaration</span></span>

1.  <span data-ttu-id="83a80-386">В [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) в общей библиотеке активов загрузите последние версии конфигураций электронной отчетности (ER) для декларации земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-386">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the Shared asset library, download the latest versions of the Electronic reporting (ER) configurations for the land tax declaration.</span></span>

    <span data-ttu-id="83a80-387">Например, для создания декларации по земельному налогу за отчетный период 2018 года загрузите последнюю версию следующих конфигураций:</span><span class="sxs-lookup"><span data-stu-id="83a80-387">For example, to generate the land tax declaration for the year 2018 reporting period, download the latest version of the following configurations:</span></span>

    -   <span data-ttu-id="83a80-388">Модель деклараций по ОС</span><span class="sxs-lookup"><span data-stu-id="83a80-388">Assets declarations model</span></span>

    -   <span data-ttu-id="83a80-389">Сопоставление модели декларации земельного налога</span><span class="sxs-lookup"><span data-stu-id="83a80-389">Land tax declaration model mapping</span></span>

    -   <span data-ttu-id="83a80-390">Формат расчета авансовых платежей по земельному налогу 5.06</span><span class="sxs-lookup"><span data-stu-id="83a80-390">Land tax advance calculation format 5.06</span></span>

    <span data-ttu-id="83a80-391">Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="83a80-391">For more information, see [Download Electronic reporting configurations from Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

2.  <span data-ttu-id="83a80-392">Можно передать параметры пакета управления данными для работы с декларацией налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="83a80-392">You can upload Data management package settings to work with the assessed tax declaration.</span></span> <span data-ttu-id="83a80-393">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83a80-393">Follow these steps:</span></span>

    -   <span data-ttu-id="83a80-394">В общей библиотеке активов LCS выберите **Пакет данных** как тип актива.</span><span class="sxs-lookup"><span data-stu-id="83a80-394">In the LCS Shared asset library, select **Data package** as the asset type.</span></span>

    -   <span data-ttu-id="83a80-395">Загрузите пакет с именем **RU Декларация по земельному налогу v5.06 (2018)**.</span><span class="sxs-lookup"><span data-stu-id="83a80-395">Download the package that is named **RU Land tax declaration v5.06 (2018)**.</span></span> <span data-ttu-id="83a80-396">Загружаемый файл называется **RU Land tax declaration v5.06 (2018).zip**.</span><span class="sxs-lookup"><span data-stu-id="83a80-396">The file that is downloaded is named **RU Land tax declaration v5.06 (2018).zip**.</span></span>

    -   <span data-ttu-id="83a80-397">В рабочей области **Управление данными** выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="83a80-397">In the **Data management** workspace, select **Import**.</span></span>

    -   <span data-ttu-id="83a80-398">В разделе **Сведения о задании** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="83a80-398">In the **Job details** section, set the following values:</span></span>

        -   <span data-ttu-id="83a80-399">Введите имя должности.</span><span class="sxs-lookup"><span data-stu-id="83a80-399">Enter a name for the job.</span></span>

        -   <span data-ttu-id="83a80-400">В поле **Формат исходных данных** выберите **Пакет**.</span><span class="sxs-lookup"><span data-stu-id="83a80-400">In the **Source data format** field, select **Package**.</span></span>

    -   <span data-ttu-id="83a80-401">Выберите **Отправить** рядом с полем **Отправить файл данных**, затем выберите файл **RU Land tax declaration v5.06 (2018).zip**, загруженный ранее.</span><span class="sxs-lookup"><span data-stu-id="83a80-401">Select **Upload** next to the **Upload data file** field, and then select the **RU Land tax declaration v5.06 (2018).zip** file that you downloaded earlier.</span></span>

    -   <span data-ttu-id="83a80-402">После отправки информационных объектов выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="83a80-402">After the data entities are uploaded, select **Import**.</span></span>

3.  <span data-ttu-id="83a80-403">Выберите пункты **Налог \> Настройка \> Электронные сообщения \> Обработка электронного сообщения** и проверьте обработку импортированных электронных сообщений.</span><span class="sxs-lookup"><span data-stu-id="83a80-403">Go to **Tax \> Setup \> Electronic messages \> Electronic message processing**, and validate the electronic message processing that is imported.</span></span> <span data-ttu-id="83a80-404">(Большая часть данных, которые были импортированы, представлена только на русском языке.)</span><span class="sxs-lookup"><span data-stu-id="83a80-404">(Most of the data that is imported is presented in the Russian language.)</span></span>

    | <span data-ttu-id="83a80-405">Обрабатывается</span><span class="sxs-lookup"><span data-stu-id="83a80-405">Processing</span></span>       | <span data-ttu-id="83a80-406">Код обработки</span><span class="sxs-lookup"><span data-stu-id="83a80-406">Processing code</span></span>  | <span data-ttu-id="83a80-407">Название</span><span class="sxs-lookup"><span data-stu-id="83a80-407">Name</span></span>                               |
    |----------------------|----------------------|----------------------------------------|
    | <span data-ttu-id="83a80-408">Декларация по земельному налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-408">Land tax declaration</span></span> | <span data-ttu-id="83a80-409">ЗемНалог 5.06 (2018)</span><span class="sxs-lookup"><span data-stu-id="83a80-409">ЗемНалог 5.06 (2018)</span></span> | <span data-ttu-id="83a80-410">Декларация по земельному налогу (2018)</span><span class="sxs-lookup"><span data-stu-id="83a80-410">Декларация по земельному налогу (2018)</span></span> |

4.  <span data-ttu-id="83a80-411">Настройте формат электронной отчетности, который выполняется при создании бухгалтерской отчетности в электронном формате:</span><span class="sxs-lookup"><span data-stu-id="83a80-411">Set up the ER format that is run when accounting reporting is generated in electronic format:</span></span>

5.  <span data-ttu-id="83a80-412">Откройте **Налог \> Настройка \> Электронные сообщения \> Действия обработки сообщения**.</span><span class="sxs-lookup"><span data-stu-id="83a80-412">Go to **Tax \> Setup \> Electronic messages \> Message processing actions**.</span></span>

6.  <span data-ttu-id="83a80-413">Выберите действие **Создать ZEMND 5.06**, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="83a80-413">Select the **Generate ZEMND 5.06** action, and then select **Edit**.</span></span>

7.  <span data-ttu-id="83a80-414">Задайте для параметра **Показать диалоговое окно** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83a80-414">Set the **Show dialog** option to **Yes**.</span></span>

8.  <span data-ttu-id="83a80-415">В поле **Сопоставление формата** выберите конфигурацию электронной отчетности **Формат декларации по земельному налогу 5.06**, загруженную ранее.</span><span class="sxs-lookup"><span data-stu-id="83a80-415">In the **Format mapping** field, select the **Land tax declaration format 5.06** ER configuration that you downloaded earlier.</span></span>

### <a name="generate-a-land-tax-declaration"></a><span data-ttu-id="83a80-416">Создание налоговой декларации по налогу на землю</span><span class="sxs-lookup"><span data-stu-id="83a80-416">Generate a land tax declaration</span></span>

<span data-ttu-id="83a80-417">Прежде чем можно будет создать декларацию по земельному налогу для налогового года, необходимо рассчитать регистр земельного налога для того же года и для первого квартала, второго квартала и третьего квартала того же года.</span><span class="sxs-lookup"><span data-stu-id="83a80-417">Before you can generate the land tax declaration for a tax year, you must calculate the land tax register for the same year, and for the first quarter, second quarter, and third quarter of the same year.</span></span> <span data-ttu-id="83a80-418">Сумма авансового платежа для земельного налога, экспортированная в декларацию по земельному налогу, берется из налоговых регистров, рассчитанных для первого квартала, второго квартала и третьего квартала.</span><span class="sxs-lookup"><span data-stu-id="83a80-418">The advance payment amount for land tax that is exported in the land tax declaration is taken from the tax registers that were calculated for the first quarter, second quarter, and third quarter.</span></span>

1.  <span data-ttu-id="83a80-419">Откройте **Налог \> Запросы и отчеты \> Электронные сообщения \> Электронные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="83a80-419">Go to **Tax \> Inquiries and reports \> Electronic messages \> Electronic messages**.</span></span>

2.  <span data-ttu-id="83a80-420">Выберите формат отчета, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="83a80-420">Select the report format to generate.</span></span>

    <span data-ttu-id="83a80-421">Например, чтобы создать декларацию по земельному налогу в формате XML за 2018 год, выберите **ЗемНалог 5.06 (2018)**.</span><span class="sxs-lookup"><span data-stu-id="83a80-421">For example, to generate a land tax declaration in XML format for the year 2018, select **ЗемНалог 5.06 (2018)**.</span></span>

3.  <span data-ttu-id="83a80-422">На экспресс-вкладке **Сообщения** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="83a80-422">On the **Messages** FastTab, select **New**.</span></span>

4.  <span data-ttu-id="83a80-423">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="83a80-423">In the **Run processing** dialog box, select **OK**.</span></span>

5.  <span data-ttu-id="83a80-424">Выберите созданную строку сообщения и введите описание.</span><span class="sxs-lookup"><span data-stu-id="83a80-424">Select the message line that is created, and enter a description.</span></span>

6.  <span data-ttu-id="83a80-425">Введите начальную и конечную дату для отчета.</span><span class="sxs-lookup"><span data-stu-id="83a80-425">Enter a start date and end date for the report.</span></span>

    <span data-ttu-id="83a80-426">Для создания декларации по земельному налогу введите годовой период.</span><span class="sxs-lookup"><span data-stu-id="83a80-426">To generate a land tax declaration, enter the year period.</span></span> <span data-ttu-id="83a80-427">Например, для 2019 года введите **01.01.2019** в поле **Начальная дата** и **31.12.2019** в поле **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="83a80-427">For example, for the year 2019, enter **01.01.2019** in the **From date** field and **31.12.2019** in the **To date** field.</span></span>

7.  <span data-ttu-id="83a80-428">Необязательно: для корректирующей декларации на экспресс-вкладке **Дополнительные поля сообщения** в строке для поля **CorrectionNumber** в поле **Значение поля** введите число корректировки для корректирующей декларации.</span><span class="sxs-lookup"><span data-stu-id="83a80-428">Optional: For a corrective declaration, on the **Message additional fields** FastTab, on the line for the **CorrectionNumber** field, in the **Field value** field, enter the number of the correction.</span></span>

8.  <span data-ttu-id="83a80-429">На экспресс-вкладке **Сообщения** выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="83a80-429">On the **Messages** FastTab, select **Update status**.</span></span>

9.  <span data-ttu-id="83a80-430">В диалоговом окне **Выполнить обработку** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="83a80-430">In the **Run processing** dialog box, select **OK**.</span></span>

10. <span data-ttu-id="83a80-431">Проверьте, что статус сообщения изменился на **Готово к формированию**.</span><span class="sxs-lookup"><span data-stu-id="83a80-431">Validate that the message status has been changed to **Ready to generate**.</span></span>

11. <span data-ttu-id="83a80-432">На экспресс-вкладке **Сообщения** выберите **Создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="83a80-432">On the **Messages** FastTab, select **Generate report**.</span></span>

12. <span data-ttu-id="83a80-433">В диалоговом окне **Параметры электронной отчетности** на экспресс-вкладке **Параметр** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="83a80-433">In the **Electronic reporting parameters** dialog box, on the **Parameter** FastTab, set the following values.</span></span>

    | <span data-ttu-id="83a80-434">Поле</span><span class="sxs-lookup"><span data-stu-id="83a80-434">Field</span></span>                                                        | <span data-ttu-id="83a80-435">Описание</span><span class="sxs-lookup"><span data-stu-id="83a80-435">Description</span></span>                                                                                                                             |
    |------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="83a80-436">По месту</span><span class="sxs-lookup"><span data-stu-id="83a80-436">At place of</span></span>                                                      | <span data-ttu-id="83a80-437">Выберите место, где предоставляется декларация: **Расположение земли** или **Регистрация крупнейшего налогоплательщика**.</span><span class="sxs-lookup"><span data-stu-id="83a80-437">Select the place where the declaration is submitted: **Ground location** or **Registration of the largest taxpayer**.</span></span>                       |
    | <span data-ttu-id="83a80-438">Номер корректировки</span><span class="sxs-lookup"><span data-stu-id="83a80-438">Correction number</span></span>                                                | <span data-ttu-id="83a80-439">Введите количество корректировки, если оно не было указано на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="83a80-439">Enter the number of the correction if you didn't specify it in step 7.</span></span>                                                                      |
    | <span data-ttu-id="83a80-440">Тип подписавшей стороны</span><span class="sxs-lookup"><span data-stu-id="83a80-440">Signatory type</span></span>                                                   | <span data-ttu-id="83a80-441">Выберите лицо, которое подписывает учетную отчетность: **Налогоплательщик** или **Представитель**.</span><span class="sxs-lookup"><span data-stu-id="83a80-441">Select the person who signs the accounting reporting: **Taxpayer** or **Representative**.</span></span>                                                   |
    | <span data-ttu-id="83a80-442">Имя подписавшего, отчество подписавшего, фамилия подписавшего</span><span class="sxs-lookup"><span data-stu-id="83a80-442">Signatory first name, Signatory middle name, Signatory last name</span></span> | <span data-ttu-id="83a80-443">Введите полное имя подписавшего.</span><span class="sxs-lookup"><span data-stu-id="83a80-443">Enter the full name of the signatory.</span></span>                                                                                                       |
    | <span data-ttu-id="83a80-444">Компания-представитель</span><span class="sxs-lookup"><span data-stu-id="83a80-444">Representative company</span></span>                                           | <span data-ttu-id="83a80-445">Если выбран тип подписи **Представитель** и представитель является организацией, введите название организации.</span><span class="sxs-lookup"><span data-stu-id="83a80-445">If you selected **Representative** as the signatory type, and if the representative is an organization, enter the name of the organization.</span></span> |
    | <span data-ttu-id="83a80-446">Документ представителя</span><span class="sxs-lookup"><span data-stu-id="83a80-446">Representative document</span></span>                                          | <span data-ttu-id="83a80-447">Если вы установили **Представитель** в качестве типа подписи, введите документ, подтверждающий полномочия представителя.</span><span class="sxs-lookup"><span data-stu-id="83a80-447">If you selected **Representative** as the signatory type, enter the document that confirms the representative's authority.</span></span>                  |

13. <span data-ttu-id="83a80-448">На первой экспресс-вкладке **Записи для добавления** примените фильтр для отдельных подразделений, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="83a80-448">On the first **Records to include** FastTab, apply a filter for separate divisions, if this type of filter is applicable.</span></span> <span data-ttu-id="83a80-449">В этом случае декларации будут создаваться только для выбранных отдельных подразделений.</span><span class="sxs-lookup"><span data-stu-id="83a80-449">In this case, declarations will be generated only for the selected separate divisions.</span></span>

14. <span data-ttu-id="83a80-450">На второй экспресс-вкладке **Записи для добавления** примените фильтр для налоговых органов, если этот тип фильтра доступен.</span><span class="sxs-lookup"><span data-stu-id="83a80-450">On the second **Records to include** FastTab, apply a filter for tax authorities, if this type of filter is applicable.</span></span> <span data-ttu-id="83a80-451">В этом случае декларации будут создаваться только для выбранных налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="83a80-451">In this case, declarations will be generated only for the selected tax authorities.</span></span>

15. <span data-ttu-id="83a80-452">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83a80-452">Select **OK**.</span></span>

    <span data-ttu-id="83a80-453">При создании отчета статус сообщения изменяется на **Создано**.</span><span class="sxs-lookup"><span data-stu-id="83a80-453">When the report is generated, the status of the message is changed to **Generated**.</span></span> <span data-ttu-id="83a80-454">При возникновении ошибки во время создания статус изменяется на **Техническая ошибка**.</span><span class="sxs-lookup"><span data-stu-id="83a80-454">If an error occurs during generation, the status is changed to **Technical error**.</span></span>

16.  <span data-ttu-id="83a80-455">На экспресс-вкладке **Журнал действий** просмотрите все действия пользователя для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="83a80-455">On the **Action log** FastTab, review all user actions for the current message.</span></span>

17.  <span data-ttu-id="83a80-456">Для просмотра созданного отчета выберите кнопку **Вложения** (символ скрепки) в верхнем правом углу страницы, затем выберите **Открыть** для просмотра файла.</span><span class="sxs-lookup"><span data-stu-id="83a80-456">To review the report that is generated, select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, and then select **Open** to view the file.</span></span>

<span data-ttu-id="83a80-457">Необходимо также вручную отправить созданный файл в специальное программное обеспечение независимых разработчиков для предварительного просмотра данных, обновления данных и передачи файлов декларации по земельному налогу в налоговые органы по каналам связи.</span><span class="sxs-lookup"><span data-stu-id="83a80-457">You must also manually upload the generated file to the special third-party software for data preview, data updates, and transfer of the land tax declaration files to the tax authorities through the communication channels.</span></span>

<a name="create-and-post-land-tax-ledger-transactions"></a><span data-ttu-id="83a80-458">Создание и разноска проводок ГК по земельному налогу</span><span class="sxs-lookup"><span data-stu-id="83a80-458">Create and post land tax ledger transactions</span></span>
--------------------------------------------

<span data-ttu-id="83a80-459">После расчета и утверждения налоговых регистров и создания декларации по земельному налогу можно создать проводки для начисления земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-459">After you've calculated and approved tax registers, and generated a land tax declaration, you can create transactions for land tax accruals.</span></span> <span data-ttu-id="83a80-460">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83a80-460">Following these steps.</span></span>

1.  <span data-ttu-id="83a80-461">Откройте **Основные средства (Россия) \> Журналы \> Журнал налоговых регистров**.</span><span class="sxs-lookup"><span data-stu-id="83a80-461">Go to **Fixed assets (Russia) \> Journals \> Tax register journal**.</span></span>

2.  <span data-ttu-id="83a80-462">Выберите журнал, затем выберите **Журнал ГК \> Земельный налог**.</span><span class="sxs-lookup"><span data-stu-id="83a80-462">Select the journal, and then select **Ledger journal \> Land tax**.</span></span>

3.  <span data-ttu-id="83a80-463">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="83a80-463">Select **New**.</span></span>

4.  <span data-ttu-id="83a80-464">В поле **Наименование** выберите наименование журнала земельного налога.</span><span class="sxs-lookup"><span data-stu-id="83a80-464">In the **Name** field, select the name of the land tax journal.</span></span>

5.  <span data-ttu-id="83a80-465">Выберите **Строки** для просмотра строк журнала, которые содержат проводки начисления земельного налога, которые были созданы на основании данных налогового регистра и настроек параметров для основных средств.</span><span class="sxs-lookup"><span data-stu-id="83a80-465">Select **Lines** to view the journal lines that have land tax accrual transactions that were created based on the tax register data and the settings of Fixed assets parameters.</span></span>

6.  <span data-ttu-id="83a80-466">Проверьте и разнесите журнал.</span><span class="sxs-lookup"><span data-stu-id="83a80-466">Validate and post the journal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]