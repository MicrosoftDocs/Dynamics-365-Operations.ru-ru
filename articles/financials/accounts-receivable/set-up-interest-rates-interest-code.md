---
title: Настройка процентных ставок для кода процента
description: Коды процента содержат настройки, определяющие, когда процент начисляется и как он вычисляется для просроченных счетов.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 665c58fd29fb986bf51e10f5814c4793940c0a47
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545586"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="08d41-103">Настройка процентных ставок для кода процента</span><span class="sxs-lookup"><span data-stu-id="08d41-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08d41-104">Коды процента содержат настройки, определяющие, когда процент начисляется и как он вычисляется для просроченных счетов.</span><span class="sxs-lookup"><span data-stu-id="08d41-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="08d41-105">Вы можете настроить один код процента и применять его к различными профилям разноски по клиенту, кодам выставления счетов или определенным строкам накладной.</span><span class="sxs-lookup"><span data-stu-id="08d41-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="08d41-106">При изменении данных кода процента все функции, использующие код, будут автоматически реализовать изменения в новых проводках.</span><span class="sxs-lookup"><span data-stu-id="08d41-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="08d41-107">Для каждого кода процента можно настроить два типа ставок.</span><span class="sxs-lookup"><span data-stu-id="08d41-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="08d41-108">Ставки для процентного дохода − они представляют доход, полученный за счет начисления процентов по накладным или процент-нотам.</span><span class="sxs-lookup"><span data-stu-id="08d41-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="08d41-109">Ставки для процентных платежей − они представляют расходы, выплаченные по проценту кредит-нот.</span><span class="sxs-lookup"><span data-stu-id="08d41-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="08d41-110">Оба типа ставок могут использоваться одновременно и в одном коде процента.</span><span class="sxs-lookup"><span data-stu-id="08d41-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="08d41-111">Ставки процента могут основываться на трех типах расчета:</span><span class="sxs-lookup"><span data-stu-id="08d41-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="08d41-112">Процент по процентным отношениям.</span><span class="sxs-lookup"><span data-stu-id="08d41-112">Interest by percentage.</span></span>
-   <span data-ttu-id="08d41-113">Процент по сумме.</span><span class="sxs-lookup"><span data-stu-id="08d41-113">Interest by amount.</span></span>
-   <span data-ttu-id="08d41-114">Процент по диапазону, который позволяет получить один процент или одну сумму.</span><span class="sxs-lookup"><span data-stu-id="08d41-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="08d41-115">При использовании кода процента для расчета процента создается отдельная процент-нота для каждой процентной ставки, действующей на момент просрочки платежа относительно даты проводки.</span><span class="sxs-lookup"><span data-stu-id="08d41-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="08d41-116">На вкладке **Доход** на странице **Код процента** можно настроить процентные ставки для процентного дохода.</span><span class="sxs-lookup"><span data-stu-id="08d41-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="08d41-117">Используйте вкладку **Платежи**, чтобы настроить процентные ставки, которые вы оплачиваете.</span><span class="sxs-lookup"><span data-stu-id="08d41-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="08d41-118">Процентные ставки на основе процентных отношений</span><span class="sxs-lookup"><span data-stu-id="08d41-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="08d41-119">Вы можете настроить ставки процента, которые вычисляют определенное процентное отношение.</span><span class="sxs-lookup"><span data-stu-id="08d41-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="08d41-120">Сумма процентов применяется ко всем валютам.</span><span class="sxs-lookup"><span data-stu-id="08d41-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="08d41-121">Можно ввести дополнительные ограничения суммы процентов.</span><span class="sxs-lookup"><span data-stu-id="08d41-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="08d41-122">Значение <strong>Процент</strong> выбрано\*\* <strong>в поле \*\*Рассчитать процент на основе</strong> на странице <strong>Настройка кодов процентов</strong>.</span><span class="sxs-lookup"><span data-stu-id="08d41-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="08d41-123">Например, чтобы настроить код процента, который начисляет 5% за каждые два месяца, в течение которых платеж по накладной совершается после даты платежа, введите 2 в поле **Рассчитывать процент каждые** и выберите **Месяц**.</span><span class="sxs-lookup"><span data-stu-id="08d41-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="08d41-124">Процентные ставки на основе сумм</span><span class="sxs-lookup"><span data-stu-id="08d41-124">Interest rates based on amounts</span></span>
<span data-ttu-id="08d41-125">Вы можете настроить ставки процента, которые вычисляют определенную сумму для валюты.</span><span class="sxs-lookup"><span data-stu-id="08d41-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="08d41-126">Сумма процентов указывается для каждой валюты в коде процента.</span><span class="sxs-lookup"><span data-stu-id="08d41-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="08d41-127">Можно ввести дополнительные ограничения суммы процентов.</span><span class="sxs-lookup"><span data-stu-id="08d41-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="08d41-128">Значение **Сумма** выбрано в поле **Рассчитать процент на основе** на странице **Настройка кодов процентов**.</span><span class="sxs-lookup"><span data-stu-id="08d41-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="08d41-129">Например, чтобы настроить код процента, который начисляет 25,00 за каждые 20 дней, в течение которых платеж по накладной совершается после даты платежа, введите 20 в поле **Рассчитывать процент каждые** и выберите **День**.</span><span class="sxs-lookup"><span data-stu-id="08d41-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="08d41-130">Процентные ставки на основе диапазонов</span><span class="sxs-lookup"><span data-stu-id="08d41-130">Interest rates based on ranges</span></span>
<span data-ttu-id="08d41-131">Вы можете настроить процентные ставки, которые изменяются в зависимости от суммы просрочки, числа дней просрочки или числа месяцев просрочки.</span><span class="sxs-lookup"><span data-stu-id="08d41-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="08d41-132">На вкладке **Прибыль по валюте** можно задать определенные параметры процентов для каждой валюты.</span><span class="sxs-lookup"><span data-stu-id="08d41-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="08d41-133">Здесь также можно определить диапазон.</span><span class="sxs-lookup"><span data-stu-id="08d41-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="08d41-134">Нажмите кнопку **Диапазоны**, чтобы добавить строки, представляющие диапазоны, которые требуется настроить.</span><span class="sxs-lookup"><span data-stu-id="08d41-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="08d41-135">Значение **От** представляет начало диапазона, а число **Сумма процентов** представляет либо процент, либо сумму в зависимости от выбора в поле **Рассчитать процент на основе** на странице **Настройка кодов процентов**.</span><span class="sxs-lookup"><span data-stu-id="08d41-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="08d41-136">Пример 1: процент по диапазону = сумма</span><span class="sxs-lookup"><span data-stu-id="08d41-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="08d41-137">Вы настраиваете код процента, который начисляет процент один раз за каждые три месяца, в течение которых платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="08d41-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="08d41-138">Вы хотите, чтобы расчет был основан на процентном отношении в соответствии с последовательными интервалами сумм.</span><span class="sxs-lookup"><span data-stu-id="08d41-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="08d41-139">Значение процента будет равно 1% для сумм накладной до 1 000,00, 2% для сумм с 1 001,00 до 5 000,00 и 3% для сумм больше 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="08d41-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="08d41-140">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="08d41-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="08d41-141">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-141">**Field name**</span></span>                  | <span data-ttu-id="08d41-142">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="08d41-143">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="08d41-143">**Interest code**</span></span>               | <span data-ttu-id="08d41-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="08d41-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="08d41-145">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="08d41-145">**Calculate interest every**</span></span>    | <span data-ttu-id="08d41-146">3/Месяц</span><span class="sxs-lookup"><span data-stu-id="08d41-146">3/Month</span></span>         |
| <span data-ttu-id="08d41-147">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="08d41-147">**Interest by range**</span></span>           | <span data-ttu-id="08d41-148">Cумма</span><span class="sxs-lookup"><span data-stu-id="08d41-148">Amount</span></span>          |
| <span data-ttu-id="08d41-149">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="08d41-149">**Calculate interest based on**</span></span> | <span data-ttu-id="08d41-150">Процент</span><span class="sxs-lookup"><span data-stu-id="08d41-150">Percentage</span></span>      |

<span data-ttu-id="08d41-151">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="08d41-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="08d41-152">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="08d41-152">**From value**</span></span> | <span data-ttu-id="08d41-153">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="08d41-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="08d41-154">0</span><span class="sxs-lookup"><span data-stu-id="08d41-154">0</span></span>              | <span data-ttu-id="08d41-155">1</span><span class="sxs-lookup"><span data-stu-id="08d41-155">1</span></span>                  |
| <span data-ttu-id="08d41-156">1,001</span><span class="sxs-lookup"><span data-stu-id="08d41-156">1,001</span></span>          | <span data-ttu-id="08d41-157">2</span><span class="sxs-lookup"><span data-stu-id="08d41-157">2</span></span>                  |
| <span data-ttu-id="08d41-158">5,001</span><span class="sxs-lookup"><span data-stu-id="08d41-158">5,001</span></span>          | <span data-ttu-id="08d41-159">3</span><span class="sxs-lookup"><span data-stu-id="08d41-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="08d41-160">Пример 2: процент по диапазону = дни</span><span class="sxs-lookup"><span data-stu-id="08d41-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="08d41-161">Вы настраиваете код процента, который начисляет процент один раз за каждые 15 дней, в течение которых платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="08d41-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="08d41-162">Вы хотите, чтобы расчет был основан на значении суммы в соответствии с последовательными интервалами дней.</span><span class="sxs-lookup"><span data-stu-id="08d41-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="08d41-163">Значение процента будет равно 10,00 за 15 дней в течение первых 60 дней, 15,00 за 15 дней в течение дней 61-90 и 20,00 за 15 дней с 91 дня и последующих дней.</span><span class="sxs-lookup"><span data-stu-id="08d41-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="08d41-164">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="08d41-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="08d41-165">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-165">**Field name**</span></span>                  | <span data-ttu-id="08d41-166">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="08d41-167">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="08d41-167">**Interest code**</span></span>               | <span data-ttu-id="08d41-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="08d41-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="08d41-169">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="08d41-169">**Calculate interest every**</span></span>    | <span data-ttu-id="08d41-170">15/День</span><span class="sxs-lookup"><span data-stu-id="08d41-170">15/Day</span></span>          |
| <span data-ttu-id="08d41-171">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="08d41-171">**Interest by range**</span></span>           | <span data-ttu-id="08d41-172">Дни</span><span class="sxs-lookup"><span data-stu-id="08d41-172">Days</span></span>            |
| <span data-ttu-id="08d41-173">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="08d41-173">**Calculate interest based on**</span></span> | <span data-ttu-id="08d41-174">Cумма</span><span class="sxs-lookup"><span data-stu-id="08d41-174">Amount</span></span>          |

<span data-ttu-id="08d41-175">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="08d41-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="08d41-176">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="08d41-176">**From value**</span></span> | <span data-ttu-id="08d41-177">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="08d41-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="08d41-178">0</span><span class="sxs-lookup"><span data-stu-id="08d41-178">0</span></span>              | <span data-ttu-id="08d41-179">10</span><span class="sxs-lookup"><span data-stu-id="08d41-179">10</span></span>                 |
| <span data-ttu-id="08d41-180">61</span><span class="sxs-lookup"><span data-stu-id="08d41-180">61</span></span>             | <span data-ttu-id="08d41-181">15</span><span class="sxs-lookup"><span data-stu-id="08d41-181">15</span></span>                 |
| <span data-ttu-id="08d41-182">91</span><span class="sxs-lookup"><span data-stu-id="08d41-182">91</span></span>             | <span data-ttu-id="08d41-183">20</span><span class="sxs-lookup"><span data-stu-id="08d41-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="08d41-184">Пример 3: процент по диапазону = месяцы</span><span class="sxs-lookup"><span data-stu-id="08d41-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="08d41-185">Вы настраиваете код процента, который начисляет процент один раз за каждый месяц, в течение которого платеж по накладной совершается после даты платежа.</span><span class="sxs-lookup"><span data-stu-id="08d41-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="08d41-186">Вы хотите, чтобы расчет был основан на процентном отношении в соответствии с последовательными интервалами месяцев.</span><span class="sxs-lookup"><span data-stu-id="08d41-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="08d41-187">Значение процента будет равно 1,5% за месяц для первых трех месяцев просрочки, 2,0% за месяц за вторые три месяца и 2,5% за каждый месяц после первых шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="08d41-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="08d41-188">Задайте следующие значения в поле кода процента.</span><span class="sxs-lookup"><span data-stu-id="08d41-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="08d41-189">**Имя поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-189">**Field name**</span></span>                  | <span data-ttu-id="08d41-190">**Значение поля**</span><span class="sxs-lookup"><span data-stu-id="08d41-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="08d41-191">**Код процента**</span><span class="sxs-lookup"><span data-stu-id="08d41-191">**Interest code**</span></span>               | <span data-ttu-id="08d41-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="08d41-192">1M%ByMth</span></span>        |
| <span data-ttu-id="08d41-193">**Рассчитывать процент каждые**</span><span class="sxs-lookup"><span data-stu-id="08d41-193">**Calculate interest every**</span></span>    | <span data-ttu-id="08d41-194">1/Месяц</span><span class="sxs-lookup"><span data-stu-id="08d41-194">1/Month</span></span>         |
| <span data-ttu-id="08d41-195">**Проценты по диапазону**</span><span class="sxs-lookup"><span data-stu-id="08d41-195">**Interest by range**</span></span>           | <span data-ttu-id="08d41-196">Месяцы</span><span class="sxs-lookup"><span data-stu-id="08d41-196">Months</span></span>          |
| <span data-ttu-id="08d41-197">**Рассчитать процент на основе**</span><span class="sxs-lookup"><span data-stu-id="08d41-197">**Calculate interest based on**</span></span> | <span data-ttu-id="08d41-198">Процент</span><span class="sxs-lookup"><span data-stu-id="08d41-198">Percentage</span></span>      |

<span data-ttu-id="08d41-199">Задайте следующие данные о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="08d41-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="08d41-200">**Со значения**</span><span class="sxs-lookup"><span data-stu-id="08d41-200">**From value**</span></span> | <span data-ttu-id="08d41-201">**Сумма процентов**</span><span class="sxs-lookup"><span data-stu-id="08d41-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="08d41-202">0</span><span class="sxs-lookup"><span data-stu-id="08d41-202">0</span></span>              | <span data-ttu-id="08d41-203">1.5</span><span class="sxs-lookup"><span data-stu-id="08d41-203">1.5</span></span>                |
| <span data-ttu-id="08d41-204">4</span><span class="sxs-lookup"><span data-stu-id="08d41-204">4</span></span>              | <span data-ttu-id="08d41-205">2</span><span class="sxs-lookup"><span data-stu-id="08d41-205">2</span></span>                  |
| <span data-ttu-id="08d41-206">7</span><span class="sxs-lookup"><span data-stu-id="08d41-206">7</span></span>              | <span data-ttu-id="08d41-207">2,5</span><span class="sxs-lookup"><span data-stu-id="08d41-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="08d41-208">Новые версии</span><span class="sxs-lookup"><span data-stu-id="08d41-208">New versions</span></span>
<span data-ttu-id="08d41-209">Коды процентов имеют даты вступления в силу.</span><span class="sxs-lookup"><span data-stu-id="08d41-209">Interest codes are date effective.</span></span> <span data-ttu-id="08d41-210">Если требуется изменить процентную ставку, моно создать **новую версию**, которая вступит в силу в будущем.</span><span class="sxs-lookup"><span data-stu-id="08d41-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="08d41-211">Чтобы просмотреть другие версии, можно использовать меню **По состоянию на**, чтобы выбрать дату прекращения.</span><span class="sxs-lookup"><span data-stu-id="08d41-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="08d41-212">Также можно выбрать значение **Отобразить все записи**, чтобы просмотреть все коды процентов на странице.</span><span class="sxs-lookup"><span data-stu-id="08d41-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



