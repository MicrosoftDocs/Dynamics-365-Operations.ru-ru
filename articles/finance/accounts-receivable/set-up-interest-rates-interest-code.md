---
title: Настройка процентных ставок для кода процента
description: Коды процента содержат настройки, определяющие, когда процент начисляется и как он вычисляется для просроченных счетов.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62868c30d3ff60e51d99c71b743ab0bbb3c87451
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835204"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="540c1-103">Настройка процентных ставок для кода процента</span><span class="sxs-lookup"><span data-stu-id="540c1-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="540c1-104">Коды процента содержат настройки, определяющие, когда процент начисляется и как он вычисляется для просроченных счетов.</span><span class="sxs-lookup"><span data-stu-id="540c1-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="540c1-105">Вы можете настроить один код процента и применять его к различными профилям разноски по клиенту, кодам выставления счетов или определенным строкам накладной.</span><span class="sxs-lookup"><span data-stu-id="540c1-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="540c1-106">При изменении данных кода процента все функции, использующие код, будут автоматически реализовать изменения в новых проводках.</span><span class="sxs-lookup"><span data-stu-id="540c1-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="540c1-107">Для каждого кода процента можно настроить два типа ставок.</span><span class="sxs-lookup"><span data-stu-id="540c1-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="540c1-108">Ставки для процентного дохода − они представляют доход, полученный за счет начисления процентов по накладным или процент-нотам.</span><span class="sxs-lookup"><span data-stu-id="540c1-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="540c1-109">Ставки для процентных платежей − они представляют расходы, выплаченные по проценту кредит-нот.</span><span class="sxs-lookup"><span data-stu-id="540c1-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="540c1-110">Оба типа ставок могут использоваться одновременно и в одном коде процента.</span><span class="sxs-lookup"><span data-stu-id="540c1-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="540c1-111">Ставки процента могут основываться на трех типах расчета:</span><span class="sxs-lookup"><span data-stu-id="540c1-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="540c1-112">Процент по процентным отношениям.</span><span class="sxs-lookup"><span data-stu-id="540c1-112">Interest by percentage.</span></span>
-   <span data-ttu-id="540c1-113">Процент по сумме.</span><span class="sxs-lookup"><span data-stu-id="540c1-113">Interest by amount.</span></span>
-   <span data-ttu-id="540c1-114">Процент по диапазону, который позволяет получить один процент или одну сумму.</span><span class="sxs-lookup"><span data-stu-id="540c1-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="540c1-115">При использовании кода процента для расчета процента создается отдельная процент-нота для каждой процентной ставки, действующей на момент просрочки платежа относительно даты проводки.</span><span class="sxs-lookup"><span data-stu-id="540c1-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="540c1-116">На вкладке **Доход** на странице **Код процента** можно настроить процентные ставки для процентного дохода.</span><span class="sxs-lookup"><span data-stu-id="540c1-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="540c1-117">Используйте вкладку **Платежи**, чтобы настроить процентные ставки, которые вы оплачиваете.</span><span class="sxs-lookup"><span data-stu-id="540c1-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="540c1-118">Процентные ставки на основе процентных отношений</span><span class="sxs-lookup"><span data-stu-id="540c1-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="540c1-119">Вы можете настроить ставки процента, которые вычисляют определенное процентное отношение.</span><span class="sxs-lookup"><span data-stu-id="540c1-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="540c1-120">Сумма процентов применяется ко всем валютам.</span><span class="sxs-lookup"><span data-stu-id="540c1-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="540c1-121">Можно ввести дополнительные ограничения суммы процентов.</span><span class="sxs-lookup"><span data-stu-id="540c1-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="540c1-122">Значение **Процент** выбрано в поле **Рассчитать процент на основе** на странице **Настройка кодов процентов**.</span><span class="sxs-lookup"><span data-stu-id="540c1-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="540c1-123">Например, чтобы настроить код процента, который начисляет 5% за каждые два месяца, в течение которых платеж по накладной совершается после даты платежа, введите 2 в поле **Рассчитывать процент каждые** и выберите **Месяц**.</span><span class="sxs-lookup"><span data-stu-id="540c1-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="540c1-124">Новый алгоритм расчета процент-ноты добавляется с использованием управления функциями.</span><span class="sxs-lookup"><span data-stu-id="540c1-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="540c1-125">Для использования этого алгоритма включите функцию **(GBL) Разрешить рассчитывать проценты за день как годовые проценты, деленные на 365**.</span><span class="sxs-lookup"><span data-stu-id="540c1-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="540c1-126">Дополнительные сведения о включении этой функции см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="540c1-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="540c1-127">Формула для расчета суммы процент-ноты:</span><span class="sxs-lookup"><span data-stu-id="540c1-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="540c1-128">Сумма процент-ноты = сумма задолженности \* годовой процент % / 365 \* число дней просрочки</span><span class="sxs-lookup"><span data-stu-id="540c1-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="540c1-129">Эта функция доступна в версии 10.0.18 или выше.</span><span class="sxs-lookup"><span data-stu-id="540c1-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="540c1-130">Процентные ставки на основе сумм</span><span class="sxs-lookup"><span data-stu-id="540c1-130">Interest rates based on amounts</span></span>
<span data-ttu-id="540c1-131">Вы можете настроить ставки процента, которые вычисляют определенную сумму для валюты.</span><span class="sxs-lookup"><span data-stu-id="540c1-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="540c1-132">Сумма процентов указывается для каждой валюты в коде процента.</span><span class="sxs-lookup"><span data-stu-id="540c1-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="540c1-133">Можно ввести дополнительные ограничения суммы процентов.</span><span class="sxs-lookup"><span data-stu-id="540c1-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="540c1-134">Значение **Сумма** выбрано в поле **Рассчитать процент на основе** на странице **Настройка кодов процентов**.</span><span class="sxs-lookup"><span data-stu-id="540c1-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="540c1-135">Например, чтобы настроить код процента, который начисляет 25,00 за каждые 20 дней, в течение которых платеж по накладной совершается после даты платежа, введите 20 в поле **Рассчитывать процент каждые** и выберите **День**.</span><span class="sxs-lookup"><span data-stu-id="540c1-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="540c1-136">Процентные ставки на основе диапазонов</span><span class="sxs-lookup"><span data-stu-id="540c1-136">Interest rates based on ranges</span></span>
<span data-ttu-id="540c1-137">Вы можете настроить процентные ставки, которые изменяются в зависимости от суммы просрочки, числа дней просрочки или числа месяцев просрочки.</span><span class="sxs-lookup"><span data-stu-id="540c1-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="540c1-138">На вкладке **Прибыль по валюте** можно задать определенные параметры процентов для каждой валюты.</span><span class="sxs-lookup"><span data-stu-id="540c1-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="540c1-139">Здесь также можно определить диапазон.</span><span class="sxs-lookup"><span data-stu-id="540c1-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="540c1-140">Нажмите кнопку **Диапазоны**, чтобы добавить строки, представляющие диапазоны, которые требуется настроить.</span><span class="sxs-lookup"><span data-stu-id="540c1-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="540c1-141">Значение **От** представляет начало диапазона, а число **Сумма процентов** представляет либо процент, либо сумму в зависимости от выбора в поле **Рассчитать процент на основе** на странице **Настройка кодов процентов**.</span><span class="sxs-lookup"><span data-stu-id="540c1-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="540c1-142">Пример 1: процент по диапазону = сумма</span><span class="sxs-lookup"><span data-stu-id="540c1-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="540c1-143">Вы настраиваете код процента, который начисляет процент один раз за каждые три месяца, в течение которых платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="540c1-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="540c1-144">Вы хотите, чтобы расчет был основан на процентном отношении в соответствии с последовательными интервалами сумм.</span><span class="sxs-lookup"><span data-stu-id="540c1-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="540c1-145">Значение процента будет равно 1% для сумм накладной до 1 000,00, 2% для сумм с 1 001,00 до 5 000,00 и 3% для сумм больше 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="540c1-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="540c1-146">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="540c1-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="540c1-147">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-147">**Field name**</span></span>                  | <span data-ttu-id="540c1-148">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="540c1-149">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="540c1-149">**Interest code**</span></span>               | <span data-ttu-id="540c1-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="540c1-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="540c1-151">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="540c1-151">**Calculate interest every**</span></span>    | <span data-ttu-id="540c1-152">3/Месяц</span><span class="sxs-lookup"><span data-stu-id="540c1-152">3/Month</span></span>         |
| <span data-ttu-id="540c1-153">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="540c1-153">**Interest by range**</span></span>           | <span data-ttu-id="540c1-154">Cумма</span><span class="sxs-lookup"><span data-stu-id="540c1-154">Amount</span></span>          |
| <span data-ttu-id="540c1-155">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="540c1-155">**Calculate interest based on**</span></span> | <span data-ttu-id="540c1-156">Процент</span><span class="sxs-lookup"><span data-stu-id="540c1-156">Percentage</span></span>      |

<span data-ttu-id="540c1-157">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="540c1-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="540c1-158">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="540c1-158">**From value**</span></span> | <span data-ttu-id="540c1-159">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="540c1-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="540c1-160">0</span><span class="sxs-lookup"><span data-stu-id="540c1-160">0</span></span>              | <span data-ttu-id="540c1-161">1</span><span class="sxs-lookup"><span data-stu-id="540c1-161">1</span></span>                  |
| <span data-ttu-id="540c1-162">1,001</span><span class="sxs-lookup"><span data-stu-id="540c1-162">1,001</span></span>          | <span data-ttu-id="540c1-163">2</span><span class="sxs-lookup"><span data-stu-id="540c1-163">2</span></span>                  |
| <span data-ttu-id="540c1-164">5,001</span><span class="sxs-lookup"><span data-stu-id="540c1-164">5,001</span></span>          | <span data-ttu-id="540c1-165">3</span><span class="sxs-lookup"><span data-stu-id="540c1-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="540c1-166">Пример 2: процент по диапазону = дни</span><span class="sxs-lookup"><span data-stu-id="540c1-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="540c1-167">Вы настраиваете код процента, который начисляет процент один раз за каждые 15 дней, в течение которых платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="540c1-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="540c1-168">Вы хотите, чтобы расчет был основан на значении суммы в соответствии с последовательными интервалами дней.</span><span class="sxs-lookup"><span data-stu-id="540c1-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="540c1-169">Значение процента будет равно 10,00 за 15 дней в течение первых 60 дней, 15,00 за 15 дней в течение дней 61-90 и 20,00 за 15 дней с 91 дня и последующих дней.</span><span class="sxs-lookup"><span data-stu-id="540c1-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="540c1-170">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="540c1-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="540c1-171">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-171">**Field name**</span></span>                  | <span data-ttu-id="540c1-172">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="540c1-173">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="540c1-173">**Interest code**</span></span>               | <span data-ttu-id="540c1-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="540c1-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="540c1-175">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="540c1-175">**Calculate interest every**</span></span>    | <span data-ttu-id="540c1-176">15/День</span><span class="sxs-lookup"><span data-stu-id="540c1-176">15/Day</span></span>          |
| <span data-ttu-id="540c1-177">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="540c1-177">**Interest by range**</span></span>           | <span data-ttu-id="540c1-178">Дни</span><span class="sxs-lookup"><span data-stu-id="540c1-178">Days</span></span>            |
| <span data-ttu-id="540c1-179">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="540c1-179">**Calculate interest based on**</span></span> | <span data-ttu-id="540c1-180">Cумма</span><span class="sxs-lookup"><span data-stu-id="540c1-180">Amount</span></span>          |

<span data-ttu-id="540c1-181">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="540c1-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="540c1-182">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="540c1-182">**From value**</span></span> | <span data-ttu-id="540c1-183">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="540c1-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="540c1-184">0</span><span class="sxs-lookup"><span data-stu-id="540c1-184">0</span></span>              | <span data-ttu-id="540c1-185">10</span><span class="sxs-lookup"><span data-stu-id="540c1-185">10</span></span>                 |
| <span data-ttu-id="540c1-186">61</span><span class="sxs-lookup"><span data-stu-id="540c1-186">61</span></span>             | <span data-ttu-id="540c1-187">15</span><span class="sxs-lookup"><span data-stu-id="540c1-187">15</span></span>                 |
| <span data-ttu-id="540c1-188">91</span><span class="sxs-lookup"><span data-stu-id="540c1-188">91</span></span>             | <span data-ttu-id="540c1-189">20</span><span class="sxs-lookup"><span data-stu-id="540c1-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="540c1-190">Пример 3: процент по диапазону = месяцы</span><span class="sxs-lookup"><span data-stu-id="540c1-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="540c1-191">Вы настраиваете код процента, который начисляет процент один раз за каждый месяц, в течение которого платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="540c1-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="540c1-192">Вы хотите, чтобы расчет был основан на процентном отношении в соответствии с последовательными интервалами месяцев.</span><span class="sxs-lookup"><span data-stu-id="540c1-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="540c1-193">Значение процента будет равно 1,5% за месяц для первых трех месяцев просрочки, 2,0% за месяц за вторые три месяца и 2,5% за каждый месяц после первых шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="540c1-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="540c1-194">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="540c1-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="540c1-195">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-195">**Field name**</span></span>                  | <span data-ttu-id="540c1-196">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="540c1-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="540c1-197">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="540c1-197">**Interest code**</span></span>               | <span data-ttu-id="540c1-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="540c1-198">1M%ByMth</span></span>        |
| <span data-ttu-id="540c1-199">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="540c1-199">**Calculate interest every**</span></span>    | <span data-ttu-id="540c1-200">1/Месяц</span><span class="sxs-lookup"><span data-stu-id="540c1-200">1/Month</span></span>         |
| <span data-ttu-id="540c1-201">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="540c1-201">**Interest by range**</span></span>           | <span data-ttu-id="540c1-202">Месяцы</span><span class="sxs-lookup"><span data-stu-id="540c1-202">Months</span></span>          |
| <span data-ttu-id="540c1-203">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="540c1-203">**Calculate interest based on**</span></span> | <span data-ttu-id="540c1-204">Процент</span><span class="sxs-lookup"><span data-stu-id="540c1-204">Percentage</span></span>      |

<span data-ttu-id="540c1-205">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="540c1-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="540c1-206">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="540c1-206">**From value**</span></span> | <span data-ttu-id="540c1-207">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="540c1-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="540c1-208">0</span><span class="sxs-lookup"><span data-stu-id="540c1-208">0</span></span>              | <span data-ttu-id="540c1-209">1.5</span><span class="sxs-lookup"><span data-stu-id="540c1-209">1.5</span></span>                |
| <span data-ttu-id="540c1-210">4</span><span class="sxs-lookup"><span data-stu-id="540c1-210">4</span></span>              | <span data-ttu-id="540c1-211">2</span><span class="sxs-lookup"><span data-stu-id="540c1-211">2</span></span>                  |
| <span data-ttu-id="540c1-212">7</span><span class="sxs-lookup"><span data-stu-id="540c1-212">7</span></span>              | <span data-ttu-id="540c1-213">2,5</span><span class="sxs-lookup"><span data-stu-id="540c1-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="540c1-214">Новые версии</span><span class="sxs-lookup"><span data-stu-id="540c1-214">New versions</span></span>
<span data-ttu-id="540c1-215">Коды процентов имеют даты вступления в силу.</span><span class="sxs-lookup"><span data-stu-id="540c1-215">Interest codes are date effective.</span></span> <span data-ttu-id="540c1-216">Если требуется изменить процентную ставку, моно создать **новую версию**, которая вступит в силу в будущем.</span><span class="sxs-lookup"><span data-stu-id="540c1-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="540c1-217">Чтобы просмотреть другие версии, можно использовать меню **По состоянию на**, чтобы выбрать дату прекращения.</span><span class="sxs-lookup"><span data-stu-id="540c1-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="540c1-218">Также можно выбрать значение **Отобразить все записи**, чтобы просмотреть все коды процентов на странице.</span><span class="sxs-lookup"><span data-stu-id="540c1-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
