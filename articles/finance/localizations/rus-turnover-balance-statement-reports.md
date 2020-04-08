---
title: Отчеты по оборотно-сальдовой ведомости
description: В этой теме приводятся сведения об оборотно-сальдовых ведомостях для клиентов, поставщиков и подотчетных лиц.
author: v-nadyuz
manager: AnnBe
ms.date: 03/16/2020
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
ms.openlocfilehash: 4f0331f8dc4ef2ef955821590e1876b0e3f7519f
ms.sourcegitcommit: e543350faaa3ff1217d21c8fd50cf90110df3ef2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/17/2020
ms.locfileid: "3137257"
---
# <a name="turnover-balance-statement-reports"></a><span data-ttu-id="559a4-103">Отчеты по оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="559a4-103">Turnover balance statement reports</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="559a4-104">Оборотно-сальдовые ведомости для клиента, поставщика и подотчетного лица позволяют отобразить информацию в контексте клиентов, поставщиков и подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="559a4-104">Turnover balance sheets for the customer, vendor, and advance holder let you show information in the context of customers, vendors, and advance holders.</span></span>

## <a name="customer-turnover-register"></a><span data-ttu-id="559a4-105">Оборотно-сальдовая ведомость (клиенты)</span><span class="sxs-lookup"><span data-stu-id="559a4-105">Customer turnover register</span></span>

1. <span data-ttu-id="559a4-106">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (клиенты)**.</span><span class="sxs-lookup"><span data-stu-id="559a4-106">Go to **General ledger** \> **Inquires and reports** \> **Turnover balance statement** \> **Customer turnover register**.</span></span>
2. <span data-ttu-id="559a4-107">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-107">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="559a4-108">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-108">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="559a4-109">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-109">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="559a4-110">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-110">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="559a4-111">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="559a4-111">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-112">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-112">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="559a4-113">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-113">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="559a4-114">В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="559a4-114">In the **Detail and sorting parameters** section, you can specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="559a4-115">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="559a4-115">You can also change the grouping order as you require.</span></span>
8. <span data-ttu-id="559a4-116">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-116">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-117">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-117">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

9. <span data-ttu-id="559a4-118">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-118">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
10. <span data-ttu-id="559a4-119">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="559a4-119">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
11. <span data-ttu-id="559a4-120">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="559a4-120">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
12. <span data-ttu-id="559a4-121">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="559a4-121">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-122">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="559a4-122">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

13. <span data-ttu-id="559a4-123">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="559a4-123">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="559a4-124">Установите для параметра **Детализировать сальдо** значение **Да**, чтобы отправить развернутое сальдо в оборотно-сальдовую ведомость.</span><span class="sxs-lookup"><span data-stu-id="559a4-124">Set the **Itemize balance** option to **Yes** to send the expanded balance to the turnover balance sheet.</span></span>
15. <span data-ttu-id="559a4-125">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="559a4-125">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница "Оборотно-сальдовая ведомость (клиенты)", вкладка "Общие"](media/1_Customer_turnover_register.jpg)

16.  <span data-ttu-id="559a4-127">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-127">Select **ОК** to generate the report.</span></span>

![Страница "Оборотно-сальдовая ведомость (клиенты)"](media/2_Customer_turnover_register.jpg)

>  [!NOTE]
>
>   - <span data-ttu-id="559a4-129">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="559a4-129">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
>   - <span data-ttu-id="559a4-130">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-130">Select **Select** to change the report generation parameters.</span></span>
>   - <span data-ttu-id="559a4-131">Выберите **Печать**, чтобы напечатать отчет в Microsoft SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="559a4-131">Select **Print** to print the report in Microsoft SQL Server Reporting Services (SSRS).</span></span>

   ![Отчет оборотно-сальдовой ведомости (клиенты)](media/3_Customer_turnover_register.jpg)

## <a name="vendor-turnover-register"></a><span data-ttu-id="559a4-133">Оборотно-сальдовая ведомость (поставщики)</span><span class="sxs-lookup"><span data-stu-id="559a4-133">Vendor turnover register</span></span>

1. <span data-ttu-id="559a4-134">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Оборотно-сальдовая ведомость (поставщики)**.</span><span class="sxs-lookup"><span data-stu-id="559a4-134">Go to **General ledger** \> **Inquires and reports** \> **Turnover balance statement** \> **Vendor turnover register**.</span></span>
2. <span data-ttu-id="559a4-135">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-135">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="559a4-136">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-136">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-137">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-137">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="559a4-138">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** и **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-138">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, and **Indicated currency**.</span></span>
5. <span data-ttu-id="559a4-139">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="559a4-139">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-140">Это поле активно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-140">This field is activated available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="559a4-141">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-141">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="559a4-142">В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="559a4-142">In the **Detail and sorting parameters** section, you can specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="559a4-143">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="559a4-143">You can also change the grouping order as you require.</span></span>
8. <span data-ttu-id="559a4-144">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-144">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="559a4-145">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-145">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

9. <span data-ttu-id="559a4-146">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-146">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
10. <span data-ttu-id="559a4-147">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="559a4-147">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
11. <span data-ttu-id="559a4-148">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="559a4-148">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
12. <span data-ttu-id="559a4-149">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="559a4-149">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-150">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="559a4-150">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

13. <span data-ttu-id="559a4-151">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="559a4-151">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="559a4-152">Установите для параметра **Детализировать сальдо** значение **Да**, чтобы отправить развернутое сальдо в оборотно-сальдовую ведомость.</span><span class="sxs-lookup"><span data-stu-id="559a4-152">Set the **Itemize balance** option to **Yes** to send the expanded balance to the turnover balance sheet.</span></span>
15. <span data-ttu-id="559a4-153">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="559a4-153">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница "Оборотно-сальдовая ведомость (поставщики)", вкладка "Общие"](media/4_Vendor_turnover_register.jpg)

16. <span data-ttu-id="559a4-155">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-155">Select **ОК** to generate the report.</span></span>

![Страница "Оборотно-сальдовая ведомость (поставщики)"](media/5_Vendor_turnover_register.jpg)

>  [!NOTE]
>
> - <span data-ttu-id="559a4-157">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="559a4-157">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="559a4-158">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-158">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="559a4-159">Выберите **Печать**, чтобы напечатать отчет в SSRS.</span><span class="sxs-lookup"><span data-stu-id="559a4-159">Select **Print** to print the report in SSRS.</span></span>

   ![Отчет оборотно-сальдовой ведомости (поставщики)](media/6_Vendor_turnover_register.jpg)

## <a name="advance-holder-turnover-register"></a><span data-ttu-id="559a4-161">Регистр оборотно-сальдовой ведомости по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="559a4-161">Advance holder turnover register</span></span>

1. <span data-ttu-id="559a4-162">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Регистр оборотно-сальдовой ведомости по подотчетным лицам**.</span><span class="sxs-lookup"><span data-stu-id="559a4-162">Go to **General ledger** \> **Inquires and reports** \> **Turnover balance statement** \> **Advance holder turnover register**.</span></span>
2. <span data-ttu-id="559a4-163">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-163">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="559a4-164">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-164">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-165">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-165">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="559a4-166">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-166">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="559a4-167">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="559a4-167">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-168">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-168">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="559a4-169">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-169">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="559a4-170">В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="559a4-170">In the **Detail and sorting parameters** section, you can specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="559a4-171">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="559a4-171">You can also change the grouping order as you require.</span></span>
8. <span data-ttu-id="559a4-172">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-172">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-173">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-173">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

9. <span data-ttu-id="559a4-174">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-174">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
10. <span data-ttu-id="559a4-175">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="559a4-175">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
11. <span data-ttu-id="559a4-176">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="559a4-176">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
12. <span data-ttu-id="559a4-177">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="559a4-177">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-178">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="559a4-178">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

13. <span data-ttu-id="559a4-179">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подрядчикам.</span><span class="sxs-lookup"><span data-stu-id="559a4-179">Set the **Show transactions** option to **Yes** to show the contractor transactions.</span></span>
14. <span data-ttu-id="559a4-180">Установите для параметра **Детализировать сальдо** значение **Да**, чтобы отправить развернутое сальдо в оборотно-сальдовую ведомость.</span><span class="sxs-lookup"><span data-stu-id="559a4-180">Set the **Itemize balance** option to **Yes** to send the expanded balance to the turnover balance sheet.</span></span>
15. <span data-ttu-id="559a4-181">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="559a4-181">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

16. <span data-ttu-id="559a4-182">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-182">Select **ОК** to generate the report.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="559a4-183">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="559a4-183">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="559a4-184">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-184">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="559a4-185">Выберите **Печать**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-185">Select **Print** to print the report.</span></span>

## <a name="general-ledger-report"></a><span data-ttu-id="559a4-186">Отчет по главной книге</span><span class="sxs-lookup"><span data-stu-id="559a4-186">General ledger report</span></span>

<span data-ttu-id="559a4-187">Отчет **Главная книга** предназначен для создания оборота по указанному счету, который используется в корреспонденции с другими счетами.</span><span class="sxs-lookup"><span data-stu-id="559a4-187">The **General ledger** report is designed to generate turnover on a specified account that is in correspondence with other accounts.</span></span>

1. <span data-ttu-id="559a4-188">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="559a4-188">Go to **General ledger** \> **Inquires and reports** \> **Turnover balance statement** \> **General ledger**.</span></span>
2. <span data-ttu-id="559a4-189">На вкладке **Общее** в поле **Код интервала дат** выберите код интервала из справочника интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-189">On the **General** tab, in the **Date interval code** field, select the date interval code from the date interval directory.</span></span>
3. <span data-ttu-id="559a4-190">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-190">In the **From date** and **To date** fields, select the start and end of the report generation period.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-191">Если эти поля не заданы вручную, значения вводятся на основе выбранного кода интервала дат.</span><span class="sxs-lookup"><span data-stu-id="559a4-191">If you don't manually set these fields, values are entered based on the selected date interval code.</span></span>

4. <span data-ttu-id="559a4-192">В поле **Тип валюты** выберите тип валюты для отчета: **Валюта учета**, **Валюта отчетности** или **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-192">In the **Currency type** field, select the currency type for the report: **Accounting currency**, **Reporting currency**, or **Indicated currency**.</span></span>
5. <span data-ttu-id="559a4-193">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="559a4-193">In the **Currency** field, select the transaction currency.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-194">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="559a4-194">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

6. <span data-ttu-id="559a4-195">В поле **Счет ГК** выберите счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-195">In the **Main account** field, select the account to generate the report for.</span></span>
7. <span data-ttu-id="559a4-196">В поле **Корр. счет** выберите корр. счет, для которого требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-196">In the **Corr. account** field, select the corresponding account to generate the report for.</span></span>
8. <span data-ttu-id="559a4-197">В разделе **Параметры детализации и сортировки** можно указать поля, используемые для группировки, перемещая их из списка **Доступные поля** в список **Выбранные поля**.</span><span class="sxs-lookup"><span data-stu-id="559a4-197">In the **Detail and sorting parameters** section, you can specify the fields that are used for grouping by moving them from the **Available fields** list to the **Selected fields** list.</span></span> <span data-ttu-id="559a4-198">Можно также изменить группирование, если требуется.</span><span class="sxs-lookup"><span data-stu-id="559a4-198">You can also change the grouping order as you require.</span></span>
9. <span data-ttu-id="559a4-199">В разделе **Аналитика** в полях **Соглашение**, **ExpenseAndIncomeCode** и **Работник** укажите коды аналитик, если требуется выбрать проводки с конкретными кодами для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-199">In the **Dimension** section, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, specify dimension codes if you want to select transactions that have specific codes for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="559a4-200">Если эти поля оставлены пустыми, система выберет проводки с *любым* кодом аналитики для отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-200">If you leave these fields blank, the system will select transactions that have *any* dimension code for the report.</span></span>

10. <span data-ttu-id="559a4-201">Установите для параметра **Печать разграничений** значение **Да**, чтобы просмотреть условия запроса при печати отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-201">Set the **Print ranges** option to **Yes** to view the query terms when you print the report.</span></span>
11. <span data-ttu-id="559a4-202">Установите для параметра **Удалять нулевые** значение **Да**, если не требуется печатать строк или столбцов с нулевыми (0) значениями.</span><span class="sxs-lookup"><span data-stu-id="559a4-202">Set the **Delete zero line** option to **Yes** if you don't want to print lines or columns that have 0 (zero) values.</span></span>
12. <span data-ttu-id="559a4-203">Выберите для **Итоговые счета** значение **Да** для итоговой суммы счета.</span><span class="sxs-lookup"><span data-stu-id="559a4-203">Set the **Total accounts** option to **Yes** to total the accounts.</span></span>
13. <span data-ttu-id="559a4-204">Выберите для **Только итоги** значение **Да** для просмотра только итоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="559a4-204">Set the **Totals only** option to **Yes** to view only total accounts.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="559a4-205">Этот параметр доступен только в том случае, если для параметра **Итоговые счета** указано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="559a4-205">This option is available only if you set the **Total accounts** option to **Yes**.</span></span>

14. <span data-ttu-id="559a4-206">Установите для параметра **Показать проводки** значение **Да**, чтобы отобразить проводки по подотчетным лицам.</span><span class="sxs-lookup"><span data-stu-id="559a4-206">Set the **Show transactions** option to **Yes** to show the accountable person transactions.</span></span>
15. <span data-ttu-id="559a4-207">Установите для параметра **Рассчитать сальдо** значение **Да**, чтобы рассчитать и показать сальдо в отчете.</span><span class="sxs-lookup"><span data-stu-id="559a4-207">Set the **Calculate balance** option to **Yes** to calculate and show the balance on the report.</span></span>

    ![Страница оборотно-сальдовой ведомости главной книги, вкладка "Общие"](media/7_General_ledger_turnover_balance_sheet.jpg)

16. <span data-ttu-id="559a4-209">Выберите **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-209">Select **ОК** to generate the report.</span></span>

![Страница оборотно-сальдовой ведомости главной книги](media/8_General_ledger.jpg)

> [!NOTE]
>
> - <span data-ttu-id="559a4-211">Выберите **Ваучер** для просмотра проводок ГК, создавших действие.</span><span class="sxs-lookup"><span data-stu-id="559a4-211">Select **Voucher** to view the ledger transactions that generated the activity.</span></span>
> - <span data-ttu-id="559a4-212">Щелкните **Выбрать** для изменения параметров создания отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-212">Select **Select** to change the report generation parameters.</span></span>
> - <span data-ttu-id="559a4-213">Выберите **Печать**, чтобы напечатать отчет в SSRS.</span><span class="sxs-lookup"><span data-stu-id="559a4-213">Select **Print** to print the report in SSRS.</span></span>

   ![Отчет оборотно-сальдовой ведомости главной книги](media/9_General_ledger.jpg)

## <a name="turnover-balance-statement-report-archive"></a><span data-ttu-id="559a4-215">Архив отчета по оборотно-сальдовой ведомости</span><span class="sxs-lookup"><span data-stu-id="559a4-215">Turnover balance statement report archive</span></span>

<span data-ttu-id="559a4-216">На странице **Архив отчетов** можно просматривать отчеты и загружать их в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="559a4-216">On the **Report archive** page, you can view reports and download them in Excel format.</span></span>

1. <span data-ttu-id="559a4-217">Перейдите **Главная книга** \> **Запросы и отчеты** \> **Оборотно-сальдовая ведомость** \> **Архив отчетов**.</span><span class="sxs-lookup"><span data-stu-id="559a4-217">Go to **General ledger** \> **Inquires and reports** \> **Turnover balance statement** \> **Report archive**.</span></span>
2. <span data-ttu-id="559a4-218">На странице **Архив отчетов по оборотно-сальдовой ведомости** в поле **Тип отчета** укажите тип отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-218">On the **Turnover and balance statement report archive** page, in the **Report type** field, specify the type of report.</span></span>
3. <span data-ttu-id="559a4-219">Выберите отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-219">Select the report.</span></span>

    ![Страница архива отчета по оборотно-сальдовой ведомости](media/10_Turnover_and_balance_statement_report_archive.jpg)

4. <span data-ttu-id="559a4-221">Выбор **Создать отчет** для создания нового отчета с теми же параметрами, что и выбранный отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-221">Select **New report** to generate a new report that has the same parameters as the selected report.</span></span>
5. <span data-ttu-id="559a4-222">Выберите **Вывод отчета**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="559a4-222">Select **Report output** to print the report.</span></span>
6. <span data-ttu-id="559a4-223">Выберите **Экспорт в Microsoft Excel**, чтобы открыть страницу **Экспорт в Excel**, а затем нажмите кнопку **Загрузить**, чтобы загрузить отчет в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="559a4-223">Select **Export to Microsoft Excel** to open the **Export to Excel** page, and then select **Download** to download the report in Excel format.</span></span>
7. <span data-ttu-id="559a4-224">Выберите **Просмотр** для просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="559a4-224">Select **View** to view the report.</span></span>

## <a name="pre-calculate-transactional-data"></a><span data-ttu-id="559a4-225">Предварительный расчет данных проводок</span><span class="sxs-lookup"><span data-stu-id="559a4-225">Pre-calculate transactional data</span></span>

<span data-ttu-id="559a4-226">Предварительно рассчитать данные проводок, можно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="559a4-226">By pre-calculating transactional data, you can help improve performance.</span></span>

1. <span data-ttu-id="559a4-227">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="559a4-227">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="559a4-228">На вкладке **Главная книга** в разделе **Оборотно-сальдовая ведомость** установите для параметра **Использовать предварительно рассчитанные данные** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="559a4-228">On the **Ledger** tab, in the **Turnover balance statement** section, set the **Use pre-calculated data** option to **Yes**.</span></span>
3. <span data-ttu-id="559a4-229">Выберите **Главная книга** \> **Периодические задачи** \> **Предварительно рассчитать данные проводок**.</span><span class="sxs-lookup"><span data-stu-id="559a4-229">Go to **General ledger** \> **Periodic tasks** \> **Pre-calculate transactional data**.</span></span>
4. <span data-ttu-id="559a4-230">В диалоговом окне **Предварительный расчет данных проводок** на экспресс-вкладке **Параметры** в поле **Тип отчета** выберите тип отчета:</span><span class="sxs-lookup"><span data-stu-id="559a4-230">In the **Pre-calculate transactional data** dialog box, on the **Parameters** FastTab, in the **Report type** field, select the type of the report:</span></span>

    - <span data-ttu-id="559a4-231">Оборотно-сальдовая ведомость (клиенты)</span><span class="sxs-lookup"><span data-stu-id="559a4-231">Customer turnover register</span></span>
    - <span data-ttu-id="559a4-232">Оборотно-сальдовая ведомость (поставщики)</span><span class="sxs-lookup"><span data-stu-id="559a4-232">Vendor turnover register</span></span>
    - <span data-ttu-id="559a4-233">Главная книга</span><span class="sxs-lookup"><span data-stu-id="559a4-233">General ledger</span></span>
    - <span data-ttu-id="559a4-234">Регистр оборотно-сальдовой ведомости по подотчетным лицам</span><span class="sxs-lookup"><span data-stu-id="559a4-234">Advance holder turnover register</span></span>

    ![Диалоговое окно предварительного расчета данных проводок](media/11_Pre-calculate_transactional_data.jpg)

5. <span data-ttu-id="559a4-236">Выберите **ОК** для предварительного расчета данных проводок.</span><span class="sxs-lookup"><span data-stu-id="559a4-236">Select **OK** to pre-calculate transactional data.</span></span>
