---
title: Отчеты по оборотно-сальдовой ведомости
description: В этой теме приводятся сведения об оборотно-сальдовых ведомостях для клиентов, поставщиков и подотчетных лиц.
author: v-nadyuz
manager: AnnBe
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e4b82fb15eac34cf1749e49b17e4827429f99639
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408590"
---
# <a name="turnover-balance-statement-reports"></a><span data-ttu-id="7d43c-103">Отчеты по оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="7d43c-103">Turnover balance statement reports</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="7d43c-104">Оборотно-сальдовые ведомости для клиента, поставщика и подотчетного лица позволяют отобразить информацию в контексте клиентов, поставщиков и подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="7d43c-104">Turnover balance sheets for the customer, vendor, and advance holder let you show information in the context of customers, vendors, and advance holders.</span></span>

## <a name="customer-turnover-register"></a><span data-ttu-id="7d43c-105">Оборотно-сальдовая ведомость (клиенты)</span><span class="sxs-lookup"><span data-stu-id="7d43c-105">Customer turnover register</span></span>

1. <span data-ttu-id="7d43c-106">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (клиенты)**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-106">Go to **General ledger** \> **Inquiries and reports** \> **Turnover balance statement** \> **Customer turnover register**.</span></span>
2. <span data-ttu-id="7d43c-107">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-107">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="7d43c-108">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-108">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7d43c-109">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-109">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="7d43c-110">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-110">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="7d43c-111">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="7d43c-111">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-112">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-112">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="7d43c-113">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-113">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="7d43c-114">Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-114">Select **Expand all** to view additional settlement information.</span></span>
8. <span data-ttu-id="7d43c-115">В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-115">In the **Detail and sorting parameters** section, specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="7d43c-116">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="7d43c-116">You can also change the grouping order as you require.</span></span>
9. <span data-ttu-id="7d43c-117">В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-117">In the **Financial dimensions** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify the dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-118">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-118">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

10. <span data-ttu-id="7d43c-119">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-119">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
11. <span data-ttu-id="7d43c-120">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="7d43c-120">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
12. <span data-ttu-id="7d43c-121">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-121">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
13. <span data-ttu-id="7d43c-122">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="7d43c-122">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="7d43c-123">Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.</span><span class="sxs-lookup"><span data-stu-id="7d43c-123">Set the **Itemize balance** option to **Yes** to show a detailed view of the balance columns.</span></span>
15. <span data-ttu-id="7d43c-124">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="7d43c-124">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница "Оборотно-сальдовая ведомость (клиенты)", вкладка "Общие"](media/01_Customer_turnover_register.jpg)

16.  <span data-ttu-id="7d43c-126">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-126">Select **ОК** to generate the report.</span></span>

![Страница "Оборотно-сальдовая ведомость (клиенты)"](media/02_Customer_turnover_register.jpg)

>  [!NOTE]
>
>   - <span data-ttu-id="7d43c-128">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="7d43c-128">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
>   - <span data-ttu-id="7d43c-129">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-129">Select **Select** to change the report generation parameters.</span></span>
>   - <span data-ttu-id="7d43c-130">Выберите **Печать**, чтобы напечатать отчет в Microsoft SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="7d43c-130">Select **Print** to print the report in Microsoft SQL Server Reporting Services (SSRS).</span></span>
>   - <span data-ttu-id="7d43c-131">Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.</span><span class="sxs-lookup"><span data-stu-id="7d43c-131">Select **Totals only** to show lines only for the first selected dimension.</span></span>

## <a name="vendor-turnover-register"></a><span data-ttu-id="7d43c-132">Оборотно-сальдовая ведомость (поставщики)</span><span class="sxs-lookup"><span data-stu-id="7d43c-132">Vendor turnover register</span></span>

1. <span data-ttu-id="7d43c-133">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (поставщики)**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-133">Go to **General ledger** \> **Inquiries and reports** \> **Turnover balance statement** \> **Vendor turnover register**.</span></span>
2. <span data-ttu-id="7d43c-134">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-134">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="7d43c-135">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-135">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-136">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-136">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="7d43c-137">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** и **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-137">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, and **Indicated currency**.</span></span>
5. <span data-ttu-id="7d43c-138">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="7d43c-138">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-139">Это поле активно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-139">This field is activated available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="7d43c-140">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-140">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="7d43c-141">Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-141">Select **Expand all** to view additional settlement information.</span></span>
8. <span data-ttu-id="7d43c-142">В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-142">In the **Detail and sorting parameters** section, specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="7d43c-143">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="7d43c-143">You can also change the grouping order as you require.</span></span>
9. <span data-ttu-id="7d43c-144">В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-144">In the **Financial dimensions** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify the dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7d43c-145">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-145">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

10. <span data-ttu-id="7d43c-146">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-146">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
11. <span data-ttu-id="7d43c-147">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="7d43c-147">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
12. <span data-ttu-id="7d43c-148">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-148">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
13. <span data-ttu-id="7d43c-149">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="7d43c-149">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="7d43c-150">Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.</span><span class="sxs-lookup"><span data-stu-id="7d43c-150">Set the **Itemize balance** option to **Yes** to show a detailed view of the balance columns.</span></span>
15. <span data-ttu-id="7d43c-151">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="7d43c-151">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница "Оборотно-сальдовая ведомость (поставщики)", вкладка "Общие"](media/04_Vendor_turnover_register.jpg)

16. <span data-ttu-id="7d43c-153">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-153">Select **ОК** to generate the report.</span></span>

![Страница "Оборотно-сальдовая ведомость (поставщики)"](media/05_Vendor_turnover_register.jpg)

>  [!NOTE]
>
> - <span data-ttu-id="7d43c-155">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="7d43c-155">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="7d43c-156">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-156">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="7d43c-157">Выберите **Печать**, чтобы напечатать отчет в SSRS.</span><span class="sxs-lookup"><span data-stu-id="7d43c-157">Select **Print** to print the report in SSRS.</span></span>
> - <span data-ttu-id="7d43c-158">Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.</span><span class="sxs-lookup"><span data-stu-id="7d43c-158">Select **Totals only** to show lines only for the first selected dimension.</span></span>

## <a name="advance-holder-turnover-register"></a><span data-ttu-id="7d43c-159">Регистр оборотно-сальдовой ведомости по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="7d43c-159">Advance holder turnover register</span></span>

1. <span data-ttu-id="7d43c-160">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Регистр оборотно-сальдовой ведомости по подотчетным лицам**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-160">Go to **General ledger** \> **Inquiries and reports** \> **Turnover balance statement** \> **Advance holder turnover register**.</span></span>
2. <span data-ttu-id="7d43c-161">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-161">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="7d43c-162">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-162">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-163">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-163">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="7d43c-164">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-164">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="7d43c-165">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="7d43c-165">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-166">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-166">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="7d43c-167">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-167">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="7d43c-168">Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-168">Select **Expand all** to view additional settlement information.</span></span>
8. <span data-ttu-id="7d43c-169">В разделе **Параметры детализации и сортировки** укажите поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-169">In the **Detail and sorting parameters** section, specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="7d43c-170">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="7d43c-170">You can also change the grouping order as you require.</span></span>
9. <span data-ttu-id="7d43c-171">В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-171">In the **Financial dimensions** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-172">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-172">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

10. <span data-ttu-id="7d43c-173">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-173">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
11. <span data-ttu-id="7d43c-174">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="7d43c-174">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
12. <span data-ttu-id="7d43c-175">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-175">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
13. <span data-ttu-id="7d43c-176">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="7d43c-176">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="7d43c-177">Установите для параметра **детализировать сальдо** значение **Да**, чтобы отобразить подробное представление столбцов сальдо.</span><span class="sxs-lookup"><span data-stu-id="7d43c-177">Set the **Itemize balance** option to **Yes** to show a detailed view of the balance columns.</span></span>
15. <span data-ttu-id="7d43c-178">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="7d43c-178">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

16. <span data-ttu-id="7d43c-179">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-179">Select **ОК** to generate the report.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="7d43c-180">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="7d43c-180">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="7d43c-181">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-181">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="7d43c-182">Выберите **Печать**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-182">Select **Print** to print the report.</span></span>
> - <span data-ttu-id="7d43c-183">Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.</span><span class="sxs-lookup"><span data-stu-id="7d43c-183">Select **Totals only** to show lines only for the first selected dimension.</span></span>

## <a name="general-ledger-report"></a><span data-ttu-id="7d43c-184">Отчет по главной книге</span><span class="sxs-lookup"><span data-stu-id="7d43c-184">General ledger report</span></span>

<span data-ttu-id="7d43c-185">Отчет **Главная книга** предназначен для создания оборота по указанному счету, который используется в корреспонденции с другими счетами.</span><span class="sxs-lookup"><span data-stu-id="7d43c-185">The **General ledger** report is designed to generate turnover on a specified account that is in correspondence with other accounts.</span></span>

1. <span data-ttu-id="7d43c-186">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-186">Go to **General ledger** \> **Inquiries and reports** \> **Turnover balance statement** \> **General ledger**.</span></span>
2. <span data-ttu-id="7d43c-187">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-187">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="7d43c-188">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-188">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-189">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="7d43c-189">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="7d43c-190">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-190">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="7d43c-191">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="7d43c-191">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-192">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-192">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="7d43c-193">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-193">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="7d43c-194">В поле **Корр. счет** выберите корр. счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-194">In the **Corr. account** field, select the corresponding account to generate the report for.</span></span>
8. <span data-ttu-id="7d43c-195">Чтобы просмотреть дополнительные сведения о сопоставлении, выберите **Развернуть все**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-195">Select **Expand all** to view additional settlement information.</span></span>
9. <span data-ttu-id="7d43c-196">В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-196">In the **Detail and sorting parameters** section, you can specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="7d43c-197">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="7d43c-197">You can also change the grouping order as you require.</span></span>
10. <span data-ttu-id="7d43c-198">В разделе **Финансовые аналитики** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-198">In the **Financial dimensions** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d43c-199">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-199">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

11. <span data-ttu-id="7d43c-200">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-200">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
12. <span data-ttu-id="7d43c-201">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="7d43c-201">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have zero (0) values.</span></span>
13. <span data-ttu-id="7d43c-202">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-202">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
14. <span data-ttu-id="7d43c-203">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подотчетным лицам.</span><span class="sxs-lookup"><span data-stu-id="7d43c-203">Set the **Show transactions** option to **Yes** to show the accountable person transactions.</span></span>
15. <span data-ttu-id="7d43c-204">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="7d43c-204">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница оборотно-сальдовой ведомости главной книги, вкладка "Общие"](media/7_General_ledger_turnover_balance_sheet.jpg)

16. <span data-ttu-id="7d43c-206">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-206">Select **ОК** to generate the report.</span></span>

![Страница оборотно-сальдовой ведомости главной книги](media/8_General_ledger.jpg)

> [!NOTE]
>
> - <span data-ttu-id="7d43c-208">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="7d43c-208">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="7d43c-209">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-209">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="7d43c-210">Выберите **Печать**, чтобы напечатать отчет в SSRS.</span><span class="sxs-lookup"><span data-stu-id="7d43c-210">Select **Print** to print the report in SSRS.</span></span>
> - <span data-ttu-id="7d43c-211">Выберите **Только итоги**, чтобы показывать только строки для первой выбранной аналитики.</span><span class="sxs-lookup"><span data-stu-id="7d43c-211">Select **Totals only** to show lines only for the first selected dimension.</span></span>

## <a name="turnover-balance-statement-report-archive"></a><span data-ttu-id="7d43c-212">Архив отчета по оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="7d43c-212">Turnover balance statement report archive</span></span>

<span data-ttu-id="7d43c-213">На странице **Архив отчетов** можно просматривать отчеты и загружать их в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="7d43c-213">On the **Report archive** page, you can view reports and download them in Excel format.</span></span>

1. <span data-ttu-id="7d43c-214">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Архив отчетов**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-214">Go to **General ledger** \> **Inquiries and reports** \> **Turnover balance statement** \> **Report archive**.</span></span>
2. <span data-ttu-id="7d43c-215">На странице **Архив отчетов по оборотно-сальдовой ведомости** в поле **Тип отчета** укажите тип отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-215">On the **Turnover and balance statement report archive** page, in the **Report type** field, specify the type of report.</span></span>
3. <span data-ttu-id="7d43c-216">Выберите отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-216">Select the report.</span></span>

    ![Страница архива отчета по оборотно-сальдовой ведомости](media/10_Turnover_and_balance_statement_report_archive.jpg)

4. <span data-ttu-id="7d43c-218">Выбор **Создать отчет** для создания нового отчета с теми же параметрами, что и выбранный отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-218">Select **New report** to generate a new report that has the same parameters as the selected report.</span></span>
5. <span data-ttu-id="7d43c-219">Выберите **Вывод отчета**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="7d43c-219">Select **Report output** to print the report.</span></span>
6. <span data-ttu-id="7d43c-220">Выберите **Экспорт в Microsoft Excel**, чтобы открыть страницу **Экспорт в Excel**, а затем нажмите кнопку **Загрузить**, чтобы загрузить отчет в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="7d43c-220">Select **Export to Microsoft Excel** to open the **Export to Excel** page, and then select **Download** to download the report in Excel format.</span></span>
7. <span data-ttu-id="7d43c-221">Выберите **Просмотр** для просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="7d43c-221">Select **View** to view the report.</span></span>

## <a name="pre-calculate-transactional-data"></a><span data-ttu-id="7d43c-222">Предварительный расчет данных проводок</span><span class="sxs-lookup"><span data-stu-id="7d43c-222">Pre-calculate transactional data</span></span>

<span data-ttu-id="7d43c-223">Предварительно рассчитать данные проводок, можно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="7d43c-223">By pre-calculating transactional data, you can help improve performance.</span></span>

1. <span data-ttu-id="7d43c-224">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-224">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="7d43c-225">На вкладке **Главная книга** в разделе **Оборотно-сальдовая ведомость** установите для параметра **Использовать предварительно рассчитанные данные** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-225">On the **Ledger** tab, in the **Turnover balance statement** section, set the **Use pre-calculated data** option to **Yes**.</span></span>
3. <span data-ttu-id="7d43c-226">Выберите **Главная книга** \> **Периодические задачи** \> **Предварительно рассчитать данные проводок**.</span><span class="sxs-lookup"><span data-stu-id="7d43c-226">Go to **General ledger** \> **Periodic tasks** \> **Pre-calculate transactional data**.</span></span>
4. <span data-ttu-id="7d43c-227">В диалоговом окне **Предварительный расчет данных проводок** на экспресс-вкладке **Параметры** в поле **Тип отчета** выберите тип отчета:</span><span class="sxs-lookup"><span data-stu-id="7d43c-227">In the **Pre-calculate transactional data** dialog box, on the **Parameters** FastTab, in the **Report type** field, select the type of the report:</span></span>

    - <span data-ttu-id="7d43c-228">Оборотно-сальдовая ведомость (клиенты)</span><span class="sxs-lookup"><span data-stu-id="7d43c-228">Customer turnover register</span></span>
    - <span data-ttu-id="7d43c-229">Оборотно-сальдовая ведомость (поставщики)</span><span class="sxs-lookup"><span data-stu-id="7d43c-229">Vendor turnover register</span></span>
    - <span data-ttu-id="7d43c-230">Главная книга</span><span class="sxs-lookup"><span data-stu-id="7d43c-230">General ledger</span></span>
    - <span data-ttu-id="7d43c-231">Регистр оборотно-сальдовой ведомости по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="7d43c-231">Advance holder turnover register</span></span>

    ![Диалоговое окно предварительного расчета данных проводок](media/11_Pre-calculate_transactional_data.jpg)

5. <span data-ttu-id="7d43c-233">Выберите **ОК** для предварительного расчета данных проводок.</span><span class="sxs-lookup"><span data-stu-id="7d43c-233">Select **OK** to pre-calculate transactional data.</span></span>
