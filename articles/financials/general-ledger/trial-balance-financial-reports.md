---
title: Финансовые отчеты по Оборотно-сальдовой ведомости
description: В этой статье описываются отчеты по умолчанию для оборотно-сальдовых ведомостей. В ней также описываются строительные блоки, связанные с этими отчетами, и изменение отчетов в соответствии с требованиями вашей компании.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd500c2880545ccae3cde7e2ead2fc5b83167d32
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595370"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="c6a1d-104">Финансовые отчеты по Оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="c6a1d-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6a1d-105">В этой статье описываются отчеты по умолчанию для оборотно-сальдовых ведомостей.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="c6a1d-106">В ней также описываются строительные блоки, связанные с этими отчетами, и изменение отчетов в соответствии с требованиями вашей компании.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="c6a1d-107">Отчеты по Оборотно-сальдовая ведомости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="c6a1d-108">Три отчета по оборотно-сальдовой ведомости доступны в Финансовой отчетности в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="c6a1d-109">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-109">Default report</span></span>                                 | <span data-ttu-id="c6a1d-110">Что он делает</span><span class="sxs-lookup"><span data-stu-id="c6a1d-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a1d-111">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="c6a1d-112">Предоставляет сведения о сальдо всех счетов, и включает сальдо дебита и кредита и чистой суммы этих сальдо вместе с датой проводки, ваучером и описанием журнала.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="c6a1d-113">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="c6a1d-114">Предоставляет сведения о сальдо всех счетов, и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="c6a1d-115">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="c6a1d-116">Предоставляет сведений о сальдо всех счетов и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей за текущий год и прошедший год.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="c6a1d-117">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-117">Building blocks</span></span>
<span data-ttu-id="c6a1d-118">Финансовые отчеты по Оборотно-сальдовая ведомости используют следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="c6a1d-119">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-119">Default report</span></span>                                 | <span data-ttu-id="c6a1d-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-120">Row definition</span></span>          | <span data-ttu-id="c6a1d-121">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c6a1d-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="c6a1d-122">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="c6a1d-123">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-123">Trial Balance - Default</span></span> | <span data-ttu-id="c6a1d-124">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="c6a1d-125">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="c6a1d-126">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-126">Trial Balance - Default</span></span> | <span data-ttu-id="c6a1d-127">Сводная Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="c6a1d-128">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="c6a1d-129">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-129">Trial Balance - Default</span></span> | <span data-ttu-id="c6a1d-130">Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6a1d-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="c6a1d-131">Определение строки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-131">Row definition</span></span>

<span data-ttu-id="c6a1d-132">Определение строк, оборотно-сальдовая ведомость — по умолчанию, содержит одну строку, которая извлекает все счета ГК.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="c6a1d-133">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="c6a1d-134">Когда вы осматриваете отчет, вы детализируете в одиночную строку, чтобы увидеть сведения о каждом счете.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="c6a1d-135">Вы можете изменить определение строки так, что оно включает больше деталей.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="c6a1d-136">Чтобы изменить определение строки Оборотно-сальдовая ведомость — по умолчанию так, что оно включит строки для всех счетов, выполните эти шаги.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="c6a1d-137">Щелкните **Редактировать**, потом щелкните **Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="c6a1d-138">Команда **Вставить строки из аналитик** позволяет вам выбрать аналитики, которые вы хотите иметь в вашем определении строки.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="c6a1d-139">Для этого определения строки вы будете использовать **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="c6a1d-140">Убеждайтесь, что **Счет ГК** содержит все амперсанды (&), и после этого щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="c6a1d-141">Определение строки теперь содержит все счета ГК для вашего юридического лицо по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="c6a1d-142">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="c6a1d-142">Column definition</span></span>

<span data-ttu-id="c6a1d-143">Каждый отчет по оборотно-сальдовой ведомости использует другое определение столбца.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="c6a1d-144">Эти определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="c6a1d-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="c6a1d-145">**Подробная оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="c6a1d-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="c6a1d-146">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c6a1d-147">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="c6a1d-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c6a1d-148">**ATTR (3)** – атрибуты:</span><span class="sxs-lookup"><span data-stu-id="c6a1d-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="c6a1d-149">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-149">Transaction Date</span></span>
        -   <span data-ttu-id="c6a1d-150">Операция</span><span class="sxs-lookup"><span data-stu-id="c6a1d-150">Voucher</span></span>
        -   <span data-ttu-id="c6a1d-151">Описание журнала</span><span class="sxs-lookup"><span data-stu-id="c6a1d-151">Journal Description</span></span>
    -   <span data-ttu-id="c6a1d-152">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="c6a1d-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="c6a1d-153">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="c6a1d-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="c6a1d-154">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="c6a1d-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="c6a1d-155">**Сводная Оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="c6a1d-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="c6a1d-156">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="c6a1d-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c6a1d-157">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c6a1d-158">**ATTR** – атрибут:</span><span class="sxs-lookup"><span data-stu-id="c6a1d-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="c6a1d-159">Операция</span><span class="sxs-lookup"><span data-stu-id="c6a1d-159">Voucher</span></span>
    -   <span data-ttu-id="c6a1d-160">**FD** — Финансовые данные начального сальдо</span><span class="sxs-lookup"><span data-stu-id="c6a1d-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="c6a1d-161">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="c6a1d-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="c6a1d-162">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="c6a1d-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="c6a1d-163">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="c6a1d-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="c6a1d-164">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="c6a1d-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="c6a1d-165">**Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="c6a1d-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="c6a1d-166">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="c6a1d-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c6a1d-167">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="c6a1d-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c6a1d-168">**ATTR** – атрибут</span><span class="sxs-lookup"><span data-stu-id="c6a1d-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="c6a1d-169">Операция</span><span class="sxs-lookup"><span data-stu-id="c6a1d-169">Voucher</span></span>
    -   <span data-ttu-id="c6a1d-170">**FD** — Финансовые данные начального сальдо на текущий год</span><span class="sxs-lookup"><span data-stu-id="c6a1d-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="c6a1d-171">**FD** — Финансовые данные, которые содержат только дебеты на текущий год</span><span class="sxs-lookup"><span data-stu-id="c6a1d-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="c6a1d-172">**FD** — Финансовые данные, которые содержат только кредиты на текущий год</span><span class="sxs-lookup"><span data-stu-id="c6a1d-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="c6a1d-173">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="c6a1d-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="c6a1d-174">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="c6a1d-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="c6a1d-175">**FD** — Финансовые данные, которые содержат только дебеты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="c6a1d-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="c6a1d-176">**FD** — Финансовые данные, которые содержат только кредиты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="c6a1d-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="c6a1d-177">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c6a1d-177">Additional resources</span></span>
--------

[<span data-ttu-id="c6a1d-178">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="c6a1d-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="c6a1d-179">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="c6a1d-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="c6a1d-180">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="c6a1d-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



