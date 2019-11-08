---
title: Расчет налога для строк общих журналов
description: В этой теме объясняется, как рассчитываются налоги для различных типов счетов (поставщик, клиент, книга учета и проект) в строках общего журнала.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570202"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="ca0c9-103">Расчет налога для строк общих журналов</span><span class="sxs-lookup"><span data-stu-id="ca0c9-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca0c9-104">В этой теме объясняется, как рассчитываются налоги для различных типов счетов (поставщик, клиент, книга учета и проект) в строках общего журнала.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="ca0c9-105">Процесс может быть разделен на три шага:</span><span class="sxs-lookup"><span data-stu-id="ca0c9-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="ca0c9-106">Определение направления налога.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="ca0c9-107">Определение суммы налога, которая будет храниться во временной таблице налогов.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="ca0c9-108">Определение суммы налога и счета в ваучере.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="ca0c9-109">Определение направления налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-109">Determine the sales tax direction</span></span>

<span data-ttu-id="ca0c9-110">Способ определения направления налога зависит от типа счета в ваучере.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="ca0c9-111">Направление налога определяется комбинацией типа счета и налогового кода.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="ca0c9-112">В следующих разделах возможности рассматриваются более подробно.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="ca0c9-113">Счет типа "Проект"</span><span class="sxs-lookup"><span data-stu-id="ca0c9-113">Account type is Project</span></span>

<span data-ttu-id="ca0c9-114">Если в операции имеется строка журнала, в которой тип счета — **Проект**, все строки журнала в операции применяют одинаковое направление налога.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca0c9-115">На следующем рисунке показано это правило.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-115">The following illustration shows the rule.</span></span> <span data-ttu-id="ca0c9-116">В следующих пунктах показаны возможные направления налогов для счетов проектов.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="ca0c9-117">• Если налоговый код является налогом за пользование, то направление налога будет "Налог за пользование".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca0c9-118">• Если налоговый код является освобождением от налога, то направление налога будет "Освобожденная от налогов".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca0c9-119">• Если налоговый код является внутренним НДС, то направление налога будет "Исходящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-120">• Если налоговый код является удержанием с покупателя, то направление налога будет "Исходящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-121">В противном случае направление налога — "Входящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca0c9-122">На следующей схеме показано правило в графическом виде.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-122">The following diagram illustrates the rule graphically.</span></span>

![Возможные направления налога для счетов "Проект"](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="ca0c9-124">Счет типа "Поставщик"</span><span class="sxs-lookup"><span data-stu-id="ca0c9-124">Account type is Vendor</span></span>

<span data-ttu-id="ca0c9-125">Если в операции имеется строка журнала, в которой тип счета — **Поставщик**, все строки журнала в операции применяют одинаковое направление налога.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca0c9-126">В следующих пунктах показаны возможные направления налогов для счетов поставщика.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="ca0c9-127">• Если налоговый код является освобождением от налога, то направление налога будет "Освобожденная от налогов".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca0c9-128">• Если налоговый код является внутренним НДС, то направление налога будет "Входящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca0c9-129">• Если налоговый код является удержанием с покупателя, то направление налога будет "Входящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="ca0c9-130">В противном случае направление налога — "Исходящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-131">На следующей схеме показано правило в графическом виде.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-131">The following diagram illustrates the rule graphically.</span></span>

![Возможные направления налога для счетов "Поставщик"](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="ca0c9-133">Счет типа "Клиент"</span><span class="sxs-lookup"><span data-stu-id="ca0c9-133">Account type is Customer</span></span>

<span data-ttu-id="ca0c9-134">Если в операции имеется строка журнала, в которой тип счета — **Клиент**, все строки журнала в операции применяют одинаковое направление налога.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="ca0c9-135">В следующих пунктах показаны возможные направления налогов для счетов клиентов.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="ca0c9-136">• Если налоговый код является налогом за пользование, то направление налога будет "Налог за пользование".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca0c9-137">• Если налоговый код является освобождением от налога, то направление налога будет "Освобожденная от налогов".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca0c9-138">• Если налоговый код является внутренним НДС, то направление налога будет "Исходящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-139">• Если налоговый код является удержанием с покупателя, то направление налога будет "Исходящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-140">В противном случае направление налога — "Входящий налог".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="ca0c9-141">На следующей схеме показано правило в графическом виде.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-141">The following diagram illustrates the rule graphically.</span></span>

![Возможные направления налога для счетов "Клиент"](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="ca0c9-143">Счет типа "Книга учета"</span><span class="sxs-lookup"><span data-stu-id="ca0c9-143">Account type is Ledger</span></span>

<span data-ttu-id="ca0c9-144">На следующем рисунке показано правило, которое применяется, когда в операции имеются только строки журнала с типом счета **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="ca0c9-145">В следующих пунктах показаны возможные направления налогов для счетов книги учета.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="ca0c9-146">• Если налоговый код является налогом за пользование, то направление налога будет "Налог за пользование".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="ca0c9-147">• Если налоговый код является освобождением от налога, то направление налога будет "Освобожденная от налогов".</span><span class="sxs-lookup"><span data-stu-id="ca0c9-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="ca0c9-148">В противном случае, если сумма журнала является дебетом (положительная), направление налога — входящий налог; если сумма журнала является кредитовой (отрицательной), направление налога — исходящий налог.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="ca0c9-149">На следующей схеме показано правило в графическом виде.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-149">The following diagram illustrates the rule graphically.</span></span>

![Возможные направления налога для счетов "Книга учета"](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="ca0c9-151">Переопределение направления налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-151">Override the sales tax direction</span></span>

<span data-ttu-id="ca0c9-152">Направление налога можно переопределить, если операция содержит только строки с типом счета **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="ca0c9-153">Перейдите в раздел **Главная книга \> План счетов \> Счета \> Счета ГК** и выберите экспресс-вкладку **Переопределения юридического лица**.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="ca0c9-154">Определение суммы налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-154">Determine the sales tax amount</span></span>

<span data-ttu-id="ca0c9-155">В этом разделе описывается порядок расчета знака суммы налога.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Страница налоговых проводок](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="ca0c9-157">В следующей таблице показано универсальное правило для определения знака сумм налога во временной таблице налогов.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="ca0c9-158">Сумма по строке журнала</span><span class="sxs-lookup"><span data-stu-id="ca0c9-158">Journal line amount</span></span> | <span data-ttu-id="ca0c9-159">Направление налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-159">Sales tax direction</span></span>  | <span data-ttu-id="ca0c9-160">Знак суммы налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="ca0c9-161">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-161">Positive</span></span>            | <span data-ttu-id="ca0c9-162">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-162">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-163">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-163">Positive</span></span>              |
| <span data-ttu-id="ca0c9-164">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-164">Positive</span></span>            | <span data-ttu-id="ca0c9-165">Исходящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-165">Sales Tax Payable</span></span>    | <span data-ttu-id="ca0c9-166">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-166">Negative</span></span>              |
| <span data-ttu-id="ca0c9-167">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-167">Negative</span></span>            | <span data-ttu-id="ca0c9-168">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-168">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-169">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-169">Negative</span></span>              |
| <span data-ttu-id="ca0c9-170">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-170">Negative</span></span>            | <span data-ttu-id="ca0c9-171">Исходящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-171">Sales Tax Payable</span></span>    | <span data-ttu-id="ca0c9-172">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-172">Positive</span></span>              |

<span data-ttu-id="ca0c9-173">Существует специальное правило для операций , имеющих только строки **Проект** или **Книга учета**, когда налоговая группа или налоговая группа номенклатур выбрана в строке **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="ca0c9-174">Это правило управляется функцией включения независимого расчета налога для общих журналов.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="ca0c9-175">Когда эта функция отключена, сумма налога в строке **Главная книга** использует направление дебета/кредита строки **Проект**.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="ca0c9-176">Когда эта функция включена, сумма налога в строке **Главная книга** использует собственное направление дебета/кредита.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="ca0c9-177">В следующих таблицах показано правило для каждого сценария.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="ca0c9-178">**Правило, когда эта функция включена**</span><span class="sxs-lookup"><span data-stu-id="ca0c9-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="ca0c9-179">Сумма по строке журнала для проекта</span><span class="sxs-lookup"><span data-stu-id="ca0c9-179">Journal line amount of project</span></span> | <span data-ttu-id="ca0c9-180">Направление налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-180">Sales tax direction</span></span>  | <span data-ttu-id="ca0c9-181">Знак суммы налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="ca0c9-182">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-182">Positive</span></span>                       | <span data-ttu-id="ca0c9-183">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-183">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-184">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-184">Positive</span></span>              |
| <span data-ttu-id="ca0c9-185">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-185">Negative</span></span>                       | <span data-ttu-id="ca0c9-186">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-186">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-187">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-187">Negative</span></span>              |

<span data-ttu-id="ca0c9-188">**Правило, когда эта функция отключена**</span><span class="sxs-lookup"><span data-stu-id="ca0c9-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="ca0c9-189">Сумма по строке журнала для книги учета</span><span class="sxs-lookup"><span data-stu-id="ca0c9-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="ca0c9-190">Направление налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-190">Sales tax direction</span></span>  | <span data-ttu-id="ca0c9-191">Знак суммы налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="ca0c9-192">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-192">Positive</span></span>                       | <span data-ttu-id="ca0c9-193">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-193">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-194">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-194">Positive</span></span>              |
| <span data-ttu-id="ca0c9-195">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-195">Negative</span></span>                       | <span data-ttu-id="ca0c9-196">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-196">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-197">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="ca0c9-198">Определение суммы налога и счета в ваучере</span><span class="sxs-lookup"><span data-stu-id="ca0c9-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="ca0c9-199">При разноске налогов основной счет извлекается из профиля группы разноски книги учета.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="ca0c9-200">Когда налоги являются входящими, система использует счет входящего налога, указанный в профиле.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="ca0c9-201">Для исходящих налогов система использует счет исходящего налога, указанный в профиле.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="ca0c9-202">В следующей таблице показано универсальное правило.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="ca0c9-203">Направление налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-203">Sales tax direction</span></span>  | <span data-ttu-id="ca0c9-204">Знак суммы налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-204">Sales tax amount sign</span></span> | <span data-ttu-id="ca0c9-205">Счет налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-205">Sales tax account</span></span>      | <span data-ttu-id="ca0c9-206">Сумма в ваучере</span><span class="sxs-lookup"><span data-stu-id="ca0c9-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="ca0c9-207">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-207">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-208">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-208">Positive</span></span>              | <span data-ttu-id="ca0c9-209">Счет входящего налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-209">Tax Receivable Account</span></span> | <span data-ttu-id="ca0c9-210">Положительная (дебит)</span><span class="sxs-lookup"><span data-stu-id="ca0c9-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="ca0c9-211">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-211">Sales Tax Receivable</span></span> | <span data-ttu-id="ca0c9-212">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-212">Negative</span></span>              | <span data-ttu-id="ca0c9-213">Счет входящего налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-213">Tax Receivable Account</span></span> | <span data-ttu-id="ca0c9-214">Отрицательная (кредит)</span><span class="sxs-lookup"><span data-stu-id="ca0c9-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="ca0c9-215">Исходящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-215">Sales Tax Payable</span></span>    | <span data-ttu-id="ca0c9-216">Положительный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-216">Positive</span></span>              | <span data-ttu-id="ca0c9-217">Счет исходящего налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-217">Tax Payable Account</span></span>    | <span data-ttu-id="ca0c9-218">Отрицательная (кредит)</span><span class="sxs-lookup"><span data-stu-id="ca0c9-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="ca0c9-219">Исходящий налог</span><span class="sxs-lookup"><span data-stu-id="ca0c9-219">Sales Tax Payable</span></span>    | <span data-ttu-id="ca0c9-220">Отрицательный</span><span class="sxs-lookup"><span data-stu-id="ca0c9-220">Negative</span></span>              | <span data-ttu-id="ca0c9-221">Счет исходящего налога</span><span class="sxs-lookup"><span data-stu-id="ca0c9-221">Tax Payable Account</span></span>    | <span data-ttu-id="ca0c9-222">Положительная (дебит)</span><span class="sxs-lookup"><span data-stu-id="ca0c9-222">Positive (Debit)</span></span>  |
