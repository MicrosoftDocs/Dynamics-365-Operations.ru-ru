---
title: Отчеты по обороту по счету
description: В этой теме приводятся сведения об отчетах оборотов по счетам, включая ведомость оборотов лист с корреспонденцией.
author: v-nadyuz
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7bc95dcc2dc54084f5049f3a67c1dec8169a364a
ms.sourcegitcommit: 7826df6c1d3d350c80cb6bca882b26828e8b854a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "3032547"
---
# <a name="account-activity-reports"></a><span data-ttu-id="ef0ac-103">Отчеты по обороту по счету</span><span class="sxs-lookup"><span data-stu-id="ef0ac-103">Account activity reports</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="ef0ac-104">Шахматная ведомость оборотов по счетам является основным компонентом бухгалтерской отчетности.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-104">The Turnover sheet with correspondence is a basic component of the accounting reports.</span></span> <span data-ttu-id="ef0ac-105">Это многостроковая таблица, в которой содержатся сведения об активности для всех счетов в течение учетного периода.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-105">It's a multirow, multicolumn table that contains information about the activity for all accounts during the accounting period.</span></span> <span data-ttu-id="ef0ac-106">Число строк и столбцов в таблице определяется количеством номеров счетов из плана счетов, настроенного на странице **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-106">The number of rows and columns in the table is determined by the number of account numbers from the chart of accounts that you set up on the **Query** page.</span></span>

<span data-ttu-id="ef0ac-107">Верхняя строка и крайний левый столбец таблицы содержат номера счетов из плана счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-107">The top row and the leftmost column of the table contain the account numbers from the chart of accounts.</span></span> <span data-ttu-id="ef0ac-108">В пересечении строк и столбцов отображается итог по всем проводкам за данный период.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-108">The intersection of rows and columns shows the total of all transactions for the period.</span></span> <span data-ttu-id="ef0ac-109">Соответствие этих проводок определяется номерами счетов в верхней строке и крайним левым столбцом, соответствующим выбранной ячейке.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-109">The correspondence of those transactions is determined by the account numbers in the top row and the leftmost column that correspond to the selected cell.</span></span>

<span data-ttu-id="ef0ac-110">Итоговые значения для каждой строки и столбца в таблице суммируются.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-110">For each row and column in the table, the totals are summarized.</span></span> <span data-ttu-id="ef0ac-111">Сводка для каждой строки записывается в нижнюю строку таблицы, а сводка для каждого столбца записывается в самом правом столбце.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-111">The summary for each row is recorded in the bottom row of the table, and the summary for each column is recorded in the rightmost column.</span></span> <span data-ttu-id="ef0ac-112">Общая сумма дебета и кредита по обороту отображается в ячейке на пересечении нижней строки и самого правого столбца.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-112">The total amount of debit and credit turnover is shown in the cell at the intersection of the bottom row and the rightmost column.</span></span>

1. <span data-ttu-id="ef0ac-113">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборот по счету** \> **Шахматная ведомость оборотов по счетам**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-113">Go to **General ledger** \> **Inquires and reports** \> **Account activity** \> **Turnover sheet with correspondence**.</span></span>
2. <span data-ttu-id="ef0ac-114">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-114">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="ef0ac-115">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-115">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-116">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-116">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="ef0ac-117">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-117">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="ef0ac-118">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-118">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-119">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-119">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="ef0ac-120">Установите для параметра **В дебет счетов** значение **Да**, если вы хотите, чтобы дебет для выбранных счетов отображался в строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-120">Set the **To debit accounts** option to **Yes** if you want the debit for the selected accounts to appear as a header line.</span></span> <span data-ttu-id="ef0ac-121">Если задано **Нет**, дебет для выбранных счетов отображается в столбце.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-121">If this option is set to **No**, the debit for the selected accounts appears in the column.</span></span>
7. <span data-ttu-id="ef0ac-122">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-122">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-123">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-123">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

8. <span data-ttu-id="ef0ac-124">В поле **Слой разноски** выберите слой разноски.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-124">In the **Posting layer** field, select the posting layer.</span></span>
9. <span data-ttu-id="ef0ac-125">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-125">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
10. <span data-ttu-id="ef0ac-126">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-126">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
11. <span data-ttu-id="ef0ac-127">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-127">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
12. <span data-ttu-id="ef0ac-128">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-128">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-129">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-129">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

    ![Страница шахматной ведомости оборотов по счетам, вкладка "Общее"](media/1_Turnover_sheet_with_correspondence.jpg)

13. <span data-ttu-id="ef0ac-131">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-131">Select **ОК** to generate the report.</span></span>

    ![Ответ "Шахматная ведомость оборотов по счетам"](media/2_Activity_of_account.jpg)

>  <span data-ttu-id="ef0ac-133">*Примечание.*</span><span class="sxs-lookup"><span data-stu-id="ef0ac-133">*Note.*</span></span>
>
>  -  <span data-ttu-id="ef0ac-134">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-134">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
>
>  -  <span data-ttu-id="ef0ac-135">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-135">Select **Select** to change the report generation parameters.</span></span>
>
>  -  <span data-ttu-id="ef0ac-136">Выберите **Печать**, чтобы напечатать отчет в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-136">Select **Print** to print the report in Microsoft Excel.</span></span>

   ![Созданный отчет "Шахматная ведомость оборотов по счетам"](media/3_Activity_of_account.jpg)

## <a name="general-ledger-report"></a><span data-ttu-id="ef0ac-138">Отчет по главной книге</span><span class="sxs-lookup"><span data-stu-id="ef0ac-138">General ledger report</span></span>

<span data-ttu-id="ef0ac-139">Отчет **Главная книга** содержит сведения о сальдо и действии для указанного счета, передаваемого в корреспонденцию со всеми счетами в плане счетов для указанного интервала дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-139">The **General ledger** report contains information about the balances and activity for a specified account that is in correspondence with all accounts in the chart of accounts for a specified date interval.</span></span> <span data-ttu-id="ef0ac-140">Отчеты разбиваются по отчетным периодам (например, месяцам).</span><span class="sxs-lookup"><span data-stu-id="ef0ac-140">The report is broken down by reporting periods (for example, months).</span></span> <span data-ttu-id="ef0ac-141">Отдельная страница создается для каждого счета в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-141">A separate page is generated for each account in the chart of accounts.</span></span>

1. <span data-ttu-id="ef0ac-142">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборот по счету** \> **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-142">Go to **General ledger** \> **Inquires and reports** \> **Account activity** \> **General ledger**.</span></span>
2. <span data-ttu-id="ef0ac-143">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-143">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="ef0ac-144">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-144">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-145">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-145">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="ef0ac-146">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-146">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="ef0ac-147">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-147">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-148">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-148">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="ef0ac-149">В полях **Со счета ГК** и **На счет ГК** укажите диапазон счетов, для которых создается отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-149">In the **From main account** and **To main account** fields, specify the range of accounts to generate the report for.</span></span>
7. <span data-ttu-id="ef0ac-150">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-150">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-151">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-151">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

8. <span data-ttu-id="ef0ac-152">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-152">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
9. <span data-ttu-id="ef0ac-153">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-153">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
10. <span data-ttu-id="ef0ac-154">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-154">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
11. <span data-ttu-id="ef0ac-155">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-155">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-156">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-156">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

12. <span data-ttu-id="ef0ac-157">Установите для параметра **Обороты по дебету** значение **Да**, чтобы напечатать подробные обороты по счету по дебету в корреспонденции дебета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-157">Set the **Debit activity** option to **Yes** to print the detailed account turnovers in debit correspondence.</span></span>
13. <span data-ttu-id="ef0ac-158">Установите для параметра **Обороты по кредиту** значение **Да**, чтобы напечатать подробные обороты по счету по кредиту в корреспонденции дебета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-158">Set the **Credit activity** option to **Yes** to print the detailed account turnovers in credit correspondence.</span></span>
14. <span data-ttu-id="ef0ac-159">Установите для параметра **По периодам** значение **Да**, чтобы напечатать отчет по интервалу в соответствии с отчетным периодом.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-159">Set the **Use periods** option to **Yes** to print the report by interval, according to the reporting period.</span></span> <span data-ttu-id="ef0ac-160">Установите для этого параметра значение **Нет**, чтобы напечатать отчет по месяцам.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-160">Set this option to **No** to print the report by months.</span></span>

    ![Страница отчета по обороту по счету главной книги, вкладка "Общие"](media/4_General_ledger.jpg)

15. <span data-ttu-id="ef0ac-162">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-162">Select **ОК** to generate the report.</span></span>

    ![Отчет по обороту по счету главной книги](media/5_Account_activity.jpg)

> [!NOTE]
>
> - <span data-ttu-id="ef0ac-164">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-164">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="ef0ac-165">Выберите ячейку "итого", чтобы открыть проводки по всем счетам, включенным в диапазон указанного итогового счета и создавшим оборот на итоговом счете.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-165">Select the total account cell to open the transactions on all accounts that are included in the range of the specified total account, and that generated activity on the total account.</span></span>
> - <span data-ttu-id="ef0ac-166">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-166">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="ef0ac-167">Выберите **Печать**, чтобы напечатать отчет в Excel.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-167">Select **Print** to print the report in Excel.</span></span>

   ![<span data-ttu-id="ef0ac-168">Созданный отчет по обороту по счету главной книги</span><span class="sxs-lookup"><span data-stu-id="ef0ac-168">Generated General ledger account activity report</span></span> ](media/6_Account_activity.jpg)

## <a name="review-of-account-report"></a><span data-ttu-id="ef0ac-169">Просмотр отчета по счету</span><span class="sxs-lookup"><span data-stu-id="ef0ac-169">Review of account report</span></span>

<span data-ttu-id="ef0ac-170">Строки отчета **Анализ счета** содержат информацию о сальдо и обороте указанного счета, который находится в корреспонденции дебета и кредита для периода, который изучается.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-170">The rows on the **Review of account** report contain information about the balances and activity of a specified account that is in debit and credit correspondence for the period that is under review.</span></span> <span data-ttu-id="ef0ac-171">В последней строке отчета суммируются обороты.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-171">The final line of the report summarizes the activity.</span></span> <span data-ttu-id="ef0ac-172">В первой строке отчета отображается сальдо в начале периода, а в последней строке отображается сальдо на конец периода.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-172">The first row of the report shows the balance at the beginning of the period, and the last row shows the balance at the end of the period.</span></span>

1. <span data-ttu-id="ef0ac-173">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборот по счету** \> **Анализ счета**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-173">Go to **General ledger** \> **Inquires and reports** \> **Account activity** \> **Review of account**.</span></span>
2. <span data-ttu-id="ef0ac-174">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-174">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="ef0ac-175">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-175">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-176">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-176">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="ef0ac-177">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-177">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="ef0ac-178">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-178">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-179">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-179">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="ef0ac-180">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-180">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="ef0ac-181">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-181">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-182">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-182">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

8. <span data-ttu-id="ef0ac-183">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-183">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
9. <span data-ttu-id="ef0ac-184">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-184">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
10. <span data-ttu-id="ef0ac-185">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-185">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-186">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-186">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

11. <span data-ttu-id="ef0ac-187">Выберите для **Счет ГК** значение **Да** для просмотра только счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-187">Set the **Main accounts only** option to **Yes** to view only main accounts.</span></span>

    ![Отчета "Анализ счета", вкладка "Общее"](media/7_Review_of_account.jpg)

12. <span data-ttu-id="ef0ac-189">На вкладке **Записи для добавления** можно выбрать **Фильтр**, чтобы указать критерии фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-189">On the **Records to include** tab, you can select **Filter** to specify filter criteria.</span></span>
13. <span data-ttu-id="ef0ac-190">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-190">Select **ОК** to generate the report.</span></span>

![Просмотр отчета по счету](media/8_Review_of_account.jpg)

> [!NOTE]
>
> - <span data-ttu-id="ef0ac-192">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-192">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="ef0ac-193">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-193">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="ef0ac-194">Выберите **Печать**, чтобы напечатать отчет в Excel.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-194">Select **Print** to print the report in Excel.</span></span>

   ![Созданный отчета "Анализ счета"](media/9_Review_of_account.jpg)

## <a name="journal-orderaccount-activity-report"></a><span data-ttu-id="ef0ac-196">Отчет "Журнал ордер/ведомость"</span><span class="sxs-lookup"><span data-stu-id="ef0ac-196">Journal order/account activity report</span></span>

<span data-ttu-id="ef0ac-197">Отчет **Журнал ордер/ведомость** можно использовать для просмотра проводок по определенному счету.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-197">You can use the **Journal order/account activity** report to review movement on a specified account in the context of transactions.</span></span> <span data-ttu-id="ef0ac-198">Также можно просмотреть пересчет сальдо для каждой проводки.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-198">You can also review the recalculation of the balance for each transaction.</span></span>

1. <span data-ttu-id="ef0ac-199">Перейдите **Главная книга \> Запросы и отчеты \> Оборот по счету \> Журнал ордер/ведомость**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-199">Go to **General ledger \> Inquires and reports \> Account activity \> Journal order/account activity**.</span></span>
2. <span data-ttu-id="ef0ac-200">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-200">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="ef0ac-201">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-201">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-202">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-202">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="ef0ac-203">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-203">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="ef0ac-204">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-204">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-205">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-205">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="ef0ac-206">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-206">In the **Main account** field, select the account to generate the report for.</span></span> <span data-ttu-id="ef0ac-207">При выборе итогового счета отчет будет создан для проводок по всем счетам, включенным в итого.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-207">If you select a total account, the report will be generated for the transactions of all accounts that are included in the total.</span></span>
7. <span data-ttu-id="ef0ac-208">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-208">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-209">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-209">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

8.  <span data-ttu-id="ef0ac-210">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-210">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
9.  <span data-ttu-id="ef0ac-211">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-211">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
10. <span data-ttu-id="ef0ac-212">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-212">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef0ac-213">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-213">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

11. <span data-ttu-id="ef0ac-214">Установите для параметра **Обороты по дебету** значение **Да**, чтобы напечатать подробные обороты по счету по дебету в корреспонденции дебета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-214">Set the **Debit activity** option to **Yes** to print the detailed account turnovers in debit correspondence.</span></span>
12. <span data-ttu-id="ef0ac-215">Установите для параметра **Обороты по кредиту** значение **Да**, чтобы напечатать подробные обороты по счету по кредиту в корреспонденции дебета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-215">Set the **Credit activity** option to **Yes** to print the detailed account turnovers in credit correspondence.</span></span>

    ![Отчет "Журнал ордер/ведомость", вкладка "Общие"](media/10_Journal_order_account_activity.jpg)

13. <span data-ttu-id="ef0ac-217">На вкладке **Записи для добавления** можно выбрать **Фильтр**, чтобы указать критерии фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-217">On the **Records to include** tab, you can select **Filter** to specifyfilter criteria.</span></span>
14. <span data-ttu-id="ef0ac-218">Выберите **ОК**, чтобы создать отчет в Excel.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-218">Select **ОК** to generate the report in Excel.</span></span>

![Созданный отчет "Журнал ордер/ведомость"](media/11_Journal_order_and_account_activity.jpg)

> [!NOTE]
>   
> - <span data-ttu-id="ef0ac-220">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-220">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="ef0ac-221">Выберите ячейку "итого", чтобы открыть проводки по всем счетам, включенным в диапазон указанного итогового счета и создавшим оборот на итоговом счете.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-221">Select the total account cell to open the transactions on all accounts that are included in the range of the specified total account, and that generated activity on the total account.</span></span>
> - <span data-ttu-id="ef0ac-222">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-222">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="ef0ac-223">Выберите **Печать**, чтобы напечатать отчет в Excel.</span><span class="sxs-lookup"><span data-stu-id="ef0ac-223">Select **Print** to print the report in Excel.</span></span>
