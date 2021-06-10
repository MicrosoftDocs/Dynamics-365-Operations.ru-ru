---
title: Финансовые отчеты по Оборотно-сальдовой ведомости
description: В этой статье описываются отчеты по умолчанию для оборотно-сальдовых ведомостей. В ней также описываются строительные блоки, связанные с этими отчетами, и изменение отчетов в соответствии с требованиями вашей компании.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103666"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="b93d0-104">Финансовые отчеты по Оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="b93d0-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b93d0-105">В этой статье описываются отчеты по умолчанию для оборотно-сальдовых ведомостей.</span><span class="sxs-lookup"><span data-stu-id="b93d0-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="b93d0-106">В ней также описываются строительные блоки, связанные с этими отчетами, и изменение отчетов в соответствии с требованиями вашей компании.</span><span class="sxs-lookup"><span data-stu-id="b93d0-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="b93d0-107">Отчеты по Оборотно-сальдовая ведомости по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-107">Default trial balance reports</span></span>

<span data-ttu-id="b93d0-108">Три отчета по оборотно-сальдовой ведомости доступны в финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="b93d0-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="b93d0-109">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-109">Default report</span></span>                                 | <span data-ttu-id="b93d0-110">Что он делает</span><span class="sxs-lookup"><span data-stu-id="b93d0-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b93d0-111">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="b93d0-112">Предоставляет сведения о сальдо всех счетов, и включает сальдо дебита и кредита и чистой суммы этих сальдо вместе с датой проводки, ваучером и описанием журнала.</span><span class="sxs-lookup"><span data-stu-id="b93d0-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="b93d0-113">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="b93d0-114">Предоставляет сведения о сальдо всех счетов, и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей.</span><span class="sxs-lookup"><span data-stu-id="b93d0-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="b93d0-115">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="b93d0-116">Предоставляет сведений о сальдо всех счетов и включает входящие и исходящие сальдо, а также сальдо дебита и кредита вместе с чистой разницей за текущий год и прошедший год.</span><span class="sxs-lookup"><span data-stu-id="b93d0-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="b93d0-117">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="b93d0-117">Building blocks</span></span>
<span data-ttu-id="b93d0-118">Финансовые отчеты по Оборотно-сальдовая ведомости используют следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="b93d0-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="b93d0-119">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-119">Default report</span></span>                                 | <span data-ttu-id="b93d0-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="b93d0-120">Row definition</span></span>          | <span data-ttu-id="b93d0-121">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="b93d0-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="b93d0-122">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="b93d0-123">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-123">Trial Balance - Default</span></span> | <span data-ttu-id="b93d0-124">Подробный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="b93d0-125">Суммарный пробный баланс — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="b93d0-126">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-126">Trial Balance - Default</span></span> | <span data-ttu-id="b93d0-127">Сводная Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="b93d0-128">Годовое сравнение суммарного пробного баланса — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="b93d0-129">Оборотно-сальдовая ведомость — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-129">Trial Balance - Default</span></span> | <span data-ttu-id="b93d0-130">Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b93d0-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="b93d0-131">При запуске отчета **Пробный баланс** в финансовой отчетности убедитесь, что установлены флажки **Отображать строки без сумм** и **Отображать отчеты без активных строк** на вкладке **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="b93d0-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="b93d0-132">Определение строки</span><span class="sxs-lookup"><span data-stu-id="b93d0-132">Row definition</span></span>

<span data-ttu-id="b93d0-133">Определение строк, оборотно-сальдовая ведомость — по умолчанию, содержит одну строку, которая извлекает все счета ГК.</span><span class="sxs-lookup"><span data-stu-id="b93d0-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="b93d0-134">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="b93d0-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="b93d0-135">Когда вы осматриваете отчет, вы детализируете в одиночную строку, чтобы увидеть сведения о каждом счете.</span><span class="sxs-lookup"><span data-stu-id="b93d0-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="b93d0-136">Вы можете изменить определение строки так, что оно включает больше деталей.</span><span class="sxs-lookup"><span data-stu-id="b93d0-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="b93d0-137">Чтобы изменить определение строки Оборотно-сальдовая ведомость — по умолчанию так, что оно включит строки для всех счетов, выполните эти шаги.</span><span class="sxs-lookup"><span data-stu-id="b93d0-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="b93d0-138">Щелкните **Редактировать**, потом щелкните **Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="b93d0-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="b93d0-139">Команда **Вставить строки из аналитик** позволяет вам выбрать аналитики, которые вы хотите иметь в вашем определении строки.</span><span class="sxs-lookup"><span data-stu-id="b93d0-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="b93d0-140">Для этого определения строки вы будете использовать **Счет ГК**.</span><span class="sxs-lookup"><span data-stu-id="b93d0-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="b93d0-141">Убеждайтесь, что **Счет ГК** содержит все амперсанды (&), и после этого щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b93d0-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="b93d0-142">Определение строки теперь содержит все счета ГК для вашего юридического лицо по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b93d0-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="b93d0-143">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="b93d0-143">Column definition</span></span>

<span data-ttu-id="b93d0-144">Каждый отчет по оборотно-сальдовой ведомости использует другое определение столбца.</span><span class="sxs-lookup"><span data-stu-id="b93d0-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="b93d0-145">Эти определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="b93d0-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="b93d0-146">**Подробная оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="b93d0-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="b93d0-147">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="b93d0-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b93d0-148">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="b93d0-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b93d0-149">**ATTR (3)** – атрибуты:</span><span class="sxs-lookup"><span data-stu-id="b93d0-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="b93d0-150">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="b93d0-150">Transaction Date</span></span>
        -   <span data-ttu-id="b93d0-151">Операция</span><span class="sxs-lookup"><span data-stu-id="b93d0-151">Voucher</span></span>
        -   <span data-ttu-id="b93d0-152">Описание журнала</span><span class="sxs-lookup"><span data-stu-id="b93d0-152">Journal Description</span></span>
    -   <span data-ttu-id="b93d0-153">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="b93d0-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="b93d0-154">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="b93d0-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="b93d0-155">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="b93d0-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="b93d0-156">**Сводная Оборотно-сальдовая ведомость — по умолчанию, типы столбцов:**</span><span class="sxs-lookup"><span data-stu-id="b93d0-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="b93d0-157">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="b93d0-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b93d0-158">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="b93d0-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b93d0-159">**ATTR** – атрибут:</span><span class="sxs-lookup"><span data-stu-id="b93d0-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="b93d0-160">Операция</span><span class="sxs-lookup"><span data-stu-id="b93d0-160">Voucher</span></span>
    -   <span data-ttu-id="b93d0-161">**FD** — Финансовые данные начального сальдо</span><span class="sxs-lookup"><span data-stu-id="b93d0-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="b93d0-162">**FD** — Финансовые данные, которые содержат только дебеты</span><span class="sxs-lookup"><span data-stu-id="b93d0-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="b93d0-163">**FD** — Финансовые данные, которые содержат только кредиты</span><span class="sxs-lookup"><span data-stu-id="b93d0-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="b93d0-164">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="b93d0-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="b93d0-165">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="b93d0-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="b93d0-166">**Годовое сравнение сводной Оборотно-сальдовой ведомости — по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="b93d0-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="b93d0-167">**ACCT** — Коды учета</span><span class="sxs-lookup"><span data-stu-id="b93d0-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b93d0-168">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="b93d0-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b93d0-169">**ATTR** – атрибут</span><span class="sxs-lookup"><span data-stu-id="b93d0-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="b93d0-170">Операция</span><span class="sxs-lookup"><span data-stu-id="b93d0-170">Voucher</span></span>
    -   <span data-ttu-id="b93d0-171">**FD** — Финансовые данные начального сальдо на текущий год</span><span class="sxs-lookup"><span data-stu-id="b93d0-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="b93d0-172">**FD** — Финансовые данные, которые содержат только дебеты на текущий год</span><span class="sxs-lookup"><span data-stu-id="b93d0-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="b93d0-173">**FD** — Финансовые данные, которые содержат только кредиты на текущий год</span><span class="sxs-lookup"><span data-stu-id="b93d0-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="b93d0-174">**CALC** – Чистое различие</span><span class="sxs-lookup"><span data-stu-id="b93d0-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="b93d0-175">**CALC** – Исходящее сальдо</span><span class="sxs-lookup"><span data-stu-id="b93d0-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="b93d0-176">**FD** — Финансовые данные, которые содержат только дебеты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="b93d0-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="b93d0-177">**FD** — Финансовые данные, которые содержат только кредиты на прошедший год</span><span class="sxs-lookup"><span data-stu-id="b93d0-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b93d0-178">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b93d0-178">Additional resources</span></span>

[<span data-ttu-id="b93d0-179">Обзор финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="b93d0-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="b93d0-180">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="b93d0-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="b93d0-181">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="b93d0-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
