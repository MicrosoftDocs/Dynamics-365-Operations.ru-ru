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
ms.openlocfilehash: c9e8c16724364df4dd62150056299e818470aa63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "309112"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="91b4c-104">Финансовые отчеты по Оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="91b4c-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91b4c-105">В этой статье описываются отчеты по умолчанию для оборотно-сальдовых ведомостей.</span><span class="sxs-lookup"><span data-stu-id="91b4c-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="91b4c-106">В ней также описываются строительные блоки, связанные с этими отчетами, и изменение отчетов в соответствии с требованиями вашей компании.</span><span class="sxs-lookup"><span data-stu-id="91b4c-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="91b4c-107">Отчеты по Оборотно-сальдовая ведомости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="91b4c-108">Три отчета по оборотно-сальдовой ведомости доступны в Финансовой отчетности в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="91b4c-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="91b4c-109">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-109">Default report</span></span>                                 | <span data-ttu-id="91b4c-110">Что он делает</span><span class="sxs-lookup"><span data-stu-id="91b4c-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b4c-111">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="91b4c-112">Предоставляет сведения о сальдо всех счетов, и включает сальдо дебита и кредита и чистой суммы этих сальдо вместе с датой проводки, ваучером и описанием журнала.</span><span class="sxs-lookup"><span data-stu-id="91b4c-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="91b4c-113">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="91b4c-114">Предоставляет сведения о сальдо всех счетов, и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей.</span><span class="sxs-lookup"><span data-stu-id="91b4c-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="91b4c-115">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="91b4c-116">Предоставляет сведений о сальдо всех счетов и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей за текущий год и прошедший год.</span><span class="sxs-lookup"><span data-stu-id="91b4c-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="91b4c-117">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="91b4c-117">Building blocks</span></span>
<span data-ttu-id="91b4c-118">Финансовые отчеты по Оборотно-сальдовая ведомости используют следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="91b4c-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="91b4c-119">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-119">Default report</span></span>                                 | <span data-ttu-id="91b4c-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="91b4c-120">Row definition</span></span>          | <span data-ttu-id="91b4c-121">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="91b4c-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="91b4c-122">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="91b4c-123">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-123">Trial Balance - Default</span></span> | <span data-ttu-id="91b4c-124">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="91b4c-125">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="91b4c-126">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-126">Trial Balance - Default</span></span> | <span data-ttu-id="91b4c-127">Сводная Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="91b4c-128">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="91b4c-129">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-129">Trial Balance - Default</span></span> | <span data-ttu-id="91b4c-130">Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91b4c-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="91b4c-131">Определение строки</span><span class="sxs-lookup"><span data-stu-id="91b4c-131">Row definition</span></span>

<span data-ttu-id="91b4c-132">Определение строк, оборотно-сальдовая ведомость — по умолчанию, содержит одну строку, которая извлекает все счета ГК.</span><span class="sxs-lookup"><span data-stu-id="91b4c-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="91b4c-133">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="91b4c-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="91b4c-134">Когда вы осматриваете отчет, вы детализируете в одиночную строку, чтобы увидеть сведения о каждом счете.</span><span class="sxs-lookup"><span data-stu-id="91b4c-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="91b4c-135">Вы можете изменить определение строки так, что оно включает больше деталей.</span><span class="sxs-lookup"><span data-stu-id="91b4c-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="91b4c-136">Чтобы изменить определение строки Оборотно-сальдовая ведомость — по умолчанию так, что оно включит строки для всех счетов, выполните эти шаги.</span><span class="sxs-lookup"><span data-stu-id="91b4c-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="91b4c-137">Щелкните **Редактировать**, потом щелкните **Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="91b4c-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="91b4c-138">Команда **Вставить строки из аналитик** позволяет вам выбрать аналитики, которые вы хотите иметь в вашем определении строки.</span><span class="sxs-lookup"><span data-stu-id="91b4c-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="91b4c-139">Для этого определения строки вы будете использовать **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="91b4c-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="91b4c-140">Убеждайтесь, что **Счет ГК** содержит все амперсанды (&), и после этого щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91b4c-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="91b4c-141">Определение строки теперь содержит все счета ГК для вашего юридического лицо по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91b4c-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="91b4c-142">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="91b4c-142">Column definition</span></span>

<span data-ttu-id="91b4c-143">Каждый отчет по оборотно-сальдовой ведомости использует другое определение столбца.</span><span class="sxs-lookup"><span data-stu-id="91b4c-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="91b4c-144">Эти определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="91b4c-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="91b4c-145">**Подробная оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="91b4c-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="91b4c-146">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="91b4c-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="91b4c-147">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="91b4c-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="91b4c-148">**ATTR (3)** – атрибуты:</span><span class="sxs-lookup"><span data-stu-id="91b4c-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="91b4c-149">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="91b4c-149">Transaction Date</span></span>
        -   <span data-ttu-id="91b4c-150">Операция</span><span class="sxs-lookup"><span data-stu-id="91b4c-150">Voucher</span></span>
        -   <span data-ttu-id="91b4c-151">Описание журнала</span><span class="sxs-lookup"><span data-stu-id="91b4c-151">Journal Description</span></span>
    -   <span data-ttu-id="91b4c-152">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="91b4c-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="91b4c-153">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="91b4c-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="91b4c-154">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="91b4c-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="91b4c-155">**Сводная Оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="91b4c-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="91b4c-156">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="91b4c-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="91b4c-157">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="91b4c-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="91b4c-158">**ATTR** – атрибут:</span><span class="sxs-lookup"><span data-stu-id="91b4c-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="91b4c-159">Операция</span><span class="sxs-lookup"><span data-stu-id="91b4c-159">Voucher</span></span>
    -   <span data-ttu-id="91b4c-160">**FD** — Финансовые данные начального сальдо</span><span class="sxs-lookup"><span data-stu-id="91b4c-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="91b4c-161">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="91b4c-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="91b4c-162">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="91b4c-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="91b4c-163">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="91b4c-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="91b4c-164">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="91b4c-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="91b4c-165">**Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="91b4c-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="91b4c-166">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="91b4c-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="91b4c-167">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="91b4c-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="91b4c-168">**ATTR** – атрибут</span><span class="sxs-lookup"><span data-stu-id="91b4c-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="91b4c-169">Операция</span><span class="sxs-lookup"><span data-stu-id="91b4c-169">Voucher</span></span>
    -   <span data-ttu-id="91b4c-170">**FD** — Финансовые данные начального сальдо на текущий год</span><span class="sxs-lookup"><span data-stu-id="91b4c-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="91b4c-171">**FD** — Финансовые данные, которые содержат только дебеты на текущий год</span><span class="sxs-lookup"><span data-stu-id="91b4c-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="91b4c-172">**FD** — Финансовые данные, которые содержат только кредиты на текущий год</span><span class="sxs-lookup"><span data-stu-id="91b4c-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="91b4c-173">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="91b4c-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="91b4c-174">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="91b4c-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="91b4c-175">**FD** — Финансовые данные, которые содержат только дебеты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="91b4c-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="91b4c-176">**FD** — Финансовые данные, которые содержат только кредиты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="91b4c-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="91b4c-177">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91b4c-177">Additional resources</span></span>
--------

[<span data-ttu-id="91b4c-178">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="91b4c-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="91b4c-179">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="91b4c-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="91b4c-180">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="91b4c-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



