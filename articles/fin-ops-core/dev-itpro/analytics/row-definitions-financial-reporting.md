---
title: Определения строк в конструкторе финансовых отчетов
description: Определение строки — это компонент отчета или строительный блок, который указывает содержимое каждой строки в финансовом отчете.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 274fa4bd137407c504f74335291e4c8e7999625b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093273"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="bb7c2-103">Определения строк в конструкторе финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="bb7c2-103">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb7c2-104">Определение строки — это компонент отчета или строительный блок, который указывает содержимое каждой строки в финансовом отчете.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-104">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="bb7c2-105">Определения строки можно объединить с определениями столбцов, определениями дерева отчетности и определениями отчетов, чтобы создать группу строительных блоков, которую можно использовать во множестве компаний.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-105">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="bb7c2-106">Создание определения строк</span><span class="sxs-lookup"><span data-stu-id="bb7c2-106">Create a row definition</span></span>

1. <span data-ttu-id="bb7c2-107">В конструкторе отчетов в области перехода щелкните **Определения строк**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-107">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="bb7c2-108">В меню **Файл** выберите команду **Создать** и щелкните **Определение строки**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-108">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="bb7c2-109">Больше информации о содержании каждой ячейки — см. [Изменение ячеек определения строки](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="bb7c2-109">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="bb7c2-110">Открытие определения строки</span><span class="sxs-lookup"><span data-stu-id="bb7c2-110">Open a row definition</span></span>
1. <span data-ttu-id="bb7c2-111">В конструкторе отчетов в области перехода щелкните **Определения строк**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-111">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="bb7c2-112">Дважды щелкните имя определения строки, которое открыть.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-112">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="bb7c2-113">Для того, чтобы осмотреть все строительные блоки, которые связаны с определением строки, выполните правый клик определения строки, и после этого выберите **Ассоциации**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-113">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="bb7c2-114">Содержимое определения строки</span><span class="sxs-lookup"><span data-stu-id="bb7c2-114">Contents of a row definition</span></span>
<span data-ttu-id="bb7c2-115">Определение строки может содержать до 20 000 строк финансовых аналитик и может включать следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="bb7c2-115">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="bb7c2-116">Описательный текст, который добавляет смысл отчету путем создания заголовков разделов, строк и пробелов, таких как **Наличные деньги** или **Итого доход**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-116">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="bb7c2-117">Ссылки на финансовые данные, которые могут включать значения аналитик в Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="bb7c2-117">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb7c2-118">Можно задать определение строк, позволяющее извлекать данные из системы финансовой аналитики при каждом формировании отчета.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-118">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="bb7c2-119">Итоги строк и формулы, которые основаны на связанных финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="bb7c2-120">Обычно, каждая строка в определении строки содержит один из следующих типов информации:</span><span class="sxs-lookup"><span data-stu-id="bb7c2-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="bb7c2-121">Ссылки на систему финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-121">References to the financial dimensions system</span></span>
- <span data-ttu-id="bb7c2-122">Итоги или расчеты, основанные на данных.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-122">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="bb7c2-123">Форматирование</span><span class="sxs-lookup"><span data-stu-id="bb7c2-123">Formatting</span></span>

<span data-ttu-id="bb7c2-124">Существует два способа ввода сведений в определение строки:</span><span class="sxs-lookup"><span data-stu-id="bb7c2-124">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="bb7c2-125">Введите сведения о строке вручную в новое определение строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="bb7c2-126">Больше информации — см. [Изменение ячеек определения строки](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="bb7c2-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="bb7c2-127">Используйте конструктор отчетов для извлечения сведений о строке непосредственно из финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="bb7c2-128">Дополнительные сведения см. в подразделе "Связанные формулы/строки/единицы измерения" раздела [Изменение ячеек определения строки](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="bb7c2-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="bb7c2-129">Добавьте аналитик к определение строки</span><span class="sxs-lookup"><span data-stu-id="bb7c2-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="bb7c2-130">Аналитика — это пересечение данных и значений.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="bb7c2-131">Можно сгруппировать данные и значения в конструкторе отчетов.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-131">You can group data and values in report designer.</span></span> <span data-ttu-id="bb7c2-132">После этого можно классифицировать и анализировать проводки более подробно.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="bb7c2-133">Вы можете использовать диалоговое окно **Вставить строки из аналитик**, чтобы добавить множественные строки к определению строки одновременно.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="bb7c2-134">Диалоговое окно показывает один столбец для каждой аналитики.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="bb7c2-135">Следующая таблица содержит описание сведений, которые можно ввести для каждой аналитики.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="bb7c2-136">Параметр</span><span class="sxs-lookup"><span data-stu-id="bb7c2-136">Option</span></span>                | <span data-ttu-id="bb7c2-137">Описание</span><span class="sxs-lookup"><span data-stu-id="bb7c2-137">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="bb7c2-138">Аналитика</span><span class="sxs-lookup"><span data-stu-id="bb7c2-138">Dimension</span></span>             | <span data-ttu-id="bb7c2-139">Схема, которая определяет аналитику, которую добавить к определению строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="bb7c2-140">Эта схема содержит один амперсанд (&) или знак номера (\#) для каждого положения в аналитиках.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="bb7c2-141">Обычно используйте все амперсанды аналитики "Счет ГК" и все знаки решетки для других аналитик.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="bb7c2-142">Начало диапазона измерений</span><span class="sxs-lookup"><span data-stu-id="bb7c2-142">Dimension Range Start</span></span> | <span data-ttu-id="bb7c2-143">Первое значение данного измерения, для которого будет выполняться вставка в определение строк.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-143">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="bb7c2-144">Конец диапазона измерений</span><span class="sxs-lookup"><span data-stu-id="bb7c2-144">Dimension Range End</span></span>   | <span data-ttu-id="bb7c2-145">Последнее значение для этой аналитики, которое нужно добавить к определению строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-145">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="bb7c2-146">Чтобы добавить аналитики к определению строки, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-146">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="bb7c2-147">В конструкторе отчетов щелкните **Определения строк** и откройте определение строки, которое требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-148">В меню **Редактировать** щелкните **Вставить строки из аналитик**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="bb7c2-149">В диалоговом окне **Вставить строки из аналитик** в строке **Аналитики** выберите ячейку для аналитики, которую требуется перенести в определение строки, и щелкните **Все &&&**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="bb7c2-150">Чтобы ограничить определение строки определенным диапазоном значений аналитик, введите начальное значение аналитики в ячейке **Начало диапазона аналитик** и конечное значение аналитики в ячейке **Конец диапазона аналитик**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="bb7c2-151">Чтобы включить все значения для выбранного измерения, оставьте эти ячейки пустыми.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-151">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb7c2-152">Подстановочные символы (\* или ?) в диапазонах аналитик могут возвращать не все нужные результаты; это зависит от способа сортировки данных в базе данных ERP-системы.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-152">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="bb7c2-153">В поле **Начальный код строки** укажите код строки для первого значения аналитики, которое требуется добавить к определению строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="bb7c2-154">В поле **Нарастить каждую строку по** укажите зазор между последовательными кодами строк.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="bb7c2-155">Например, если первый код строки — 100 и значение приращения — 30, то первые новые строки будут иметь коды 100, 130, 160, 190 и 220.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="bb7c2-156">Используйте значение приращения, которое обеспечивает достаточно места для вставки новых строк формата и формул.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="bb7c2-157">Нажмите кнопку **OК**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-157">Click **OK**.</span></span> <span data-ttu-id="bb7c2-158">Для каждого выбранного значения аналитики добавляется одна строка к определению строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="bb7c2-159">Откорректировать округление в определении строки</span><span class="sxs-lookup"><span data-stu-id="bb7c2-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="bb7c2-160">Если имеется балансовый отчет, в котором суммы округлены, итоги могут расходиться.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="bb7c2-161">Эта проблема может возникнуть, если, например, используется параметр округления в балансовом отчете и определение отчета также указывает округление.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="bb7c2-162">Можно использовать параметр **Корректировка округления** в определении строки для балансировки сумм в балансовых отчетах.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="bb7c2-163">Можно отключить округление или изменить его на вкладке **Параметры** определения отчета.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="bb7c2-164">В следующей таблице показан способ округления сумм:</span><span class="sxs-lookup"><span data-stu-id="bb7c2-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="bb7c2-165">В этой таблице, итоги строк 100 и 200 отличаются, когда округление включено.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="bb7c2-166">Код строки</span><span class="sxs-lookup"><span data-stu-id="bb7c2-166">Row code</span></span> | <span data-ttu-id="bb7c2-167">Суммы без округления</span><span class="sxs-lookup"><span data-stu-id="bb7c2-167">Amounts without rounding</span></span> | <span data-ttu-id="bb7c2-168">Сумма с округления к целым тысячам</span><span class="sxs-lookup"><span data-stu-id="bb7c2-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="bb7c2-169">100</span><span class="sxs-lookup"><span data-stu-id="bb7c2-169">100</span></span>      | <span data-ttu-id="bb7c2-170">3600</span><span class="sxs-lookup"><span data-stu-id="bb7c2-170">3,600</span></span>                    | <span data-ttu-id="bb7c2-171">4</span><span class="sxs-lookup"><span data-stu-id="bb7c2-171">4</span></span>                                       |
| <span data-ttu-id="bb7c2-172">200</span><span class="sxs-lookup"><span data-stu-id="bb7c2-172">200</span></span>      | <span data-ttu-id="bb7c2-173">3700</span><span class="sxs-lookup"><span data-stu-id="bb7c2-173">3,700</span></span>                    | <span data-ttu-id="bb7c2-174">4</span><span class="sxs-lookup"><span data-stu-id="bb7c2-174">4</span></span>                                       |
| <span data-ttu-id="bb7c2-175">Всего</span><span class="sxs-lookup"><span data-stu-id="bb7c2-175">Total</span></span>    | <span data-ttu-id="bb7c2-176">7300</span><span class="sxs-lookup"><span data-stu-id="bb7c2-176">7,300</span></span>                    | <span data-ttu-id="bb7c2-177">8</span><span class="sxs-lookup"><span data-stu-id="bb7c2-177">8</span></span>                                       |

<span data-ttu-id="bb7c2-178">Чтобы скорректировать округление в балансовом отчете, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="bb7c2-179">В конструкторе отчетов щелкните **Определения строк**, и после этого раскройте определение строки, которое надо изменить.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-180">В меню **Правка** выберите команду **Корректировка округления**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="bb7c2-181">В диалоговом окне **Корректировка округления** введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bb7c2-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="bb7c2-182">**Строка корректировки округления** — код строки, которая будет скорректирована для того, чтобы сбалансировать балансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="bb7c2-183">**Строка общих активов** — код строки для строки в балансовом отчете, которая содержит общие активы.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="bb7c2-184">**Строка обязательств и собственного капитала** — код строки для строки в балансовом отчете, которая содержит обязательства и собственный капитал.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="bb7c2-185">**Предел суммы корректировки** — положительное целое число, которое определяет предел в автоматических корректировках.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="bb7c2-186">Эта сумма сравнивается с абсолютным значением фактической величины округления.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb7c2-187">Эти коды строк должны быть связаны с нужными финансовыми данными.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-187">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="bb7c2-188">Иными словами, строка должна содержать значение измерения в своей ячейке **Связь с финансовой аналитикой**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="bb7c2-189">**Не** ссылайтесь на строку описания (**DESC**), расчетную (**CALC**), или подытоженную строку (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="bb7c2-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="bb7c2-190">Суммы в балансовом отчете будут балансироваться равномерно, если округление включено.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="bb7c2-191">Предел корректировки применяется на основе параметра **Точность округления**, заданного для определения отчета.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-191">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="bb7c2-192">Например, если выбрать округление отчета до тысяч и ввести **2** в поле **Предел суммы корректировки**, отобразится предупреждение, когда значение в поле **Строка корректировки округления** увеличивается или уменьшается больше чем на 2 000.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="bb7c2-193">Строка формата и текст столбца</span><span class="sxs-lookup"><span data-stu-id="bb7c2-193">Format row and column text</span></span>
<span data-ttu-id="bb7c2-194">Вы можете настроить внешний вид ваших отчетов, изменив шрифты и форматируя текст</span><span class="sxs-lookup"><span data-stu-id="bb7c2-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="bb7c2-195">В следующих разделах объясняется, как отформатировать внешний вид строк и столбцов в отчетах.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="bb7c2-196">Управление стилями шрифтов</span><span class="sxs-lookup"><span data-stu-id="bb7c2-196">Manage font styles</span></span>

<span data-ttu-id="bb7c2-197">Можно создавать и изменять стили шрифтов для отчета.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="bb7c2-198">Затем эти стили можно применить к документу или к определенной строке или столбцу в отчете.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="bb7c2-199"><strong>Создайте стиль шрифта</strong></span><span class="sxs-lookup"><span data-stu-id="bb7c2-199"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="bb7c2-200">В конструкторе отчета, в меню <strong>Формат</strong>, щелкните <strong>Стили и форматирование</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="bb7c2-201">В диалоговом окне <strong>Стили и форматирование</strong> щелкните <strong>Создать</strong> и введите уникальное имя нового начертания.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="bb7c2-202">Выберите параметры шрифта и нажмите кнопку <strong>ОК</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="bb7c2-203"><strong>Изменение начертания шрифта</strong></span><span class="sxs-lookup"><span data-stu-id="bb7c2-203"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="bb7c2-204">В конструкторе отчета, в меню <strong>Формат</strong>, щелкните <strong>Стили и форматирование</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="bb7c2-205">В диалоговом окне <strong>Стили и форматирование</strong> выберите изменяемое начертание и нажмите кнопку <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="bb7c2-206">Выберите параметры шрифта и нажмите кнопку <strong>ОК</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="bb7c2-207"><strong>Применить стиль шрифта</strong></span><span class="sxs-lookup"><span data-stu-id="bb7c2-207"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="bb7c2-208">В конструкторе отчетов в определении или определении столбца либо в верхних и нижних колонтитулах выберите одну или несколько ячеек.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="bb7c2-209">В списке <strong>Стиль</strong> на панели инструментов выберите начертание шрифта.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="bb7c2-210">Текст строки формата</span><span class="sxs-lookup"><span data-stu-id="bb7c2-210">Format row text</span></span>

<span data-ttu-id="bb7c2-211">Форматирование, заданное в определении строки, переопределяет форматирование, заданное в определении столбца и в определении отчета.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="bb7c2-212">Формат текста можно изменить с помощью элементов управления на панели инструментов форматирования.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="bb7c2-213">Эти элементы являются стандартными элементами управления Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-213">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="bb7c2-214">В конструкторе отчетов выберите редактируемое определение строки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-214">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-215">Выберите ячейки, которые форматировать.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-215">Select the cells to format.</span></span> <span data-ttu-id="bb7c2-216">Чтобы выбрать несколько ячеек, удерживайте клавишу Ctrl, пока вы выбираете ячейки.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="bb7c2-217">Нажмите кнопку формата, который требуется применить, на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="bb7c2-218">Например, чтобы сделать отступ строки, выберите строку и щелкните **Увеличить отступ** ![Увеличить отступ](media/indent.gif "Увеличить отступ") на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="bb7c2-219">Отрегулируйте столбцы, когда вы конструируете отчеты</span><span class="sxs-lookup"><span data-stu-id="bb7c2-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="bb7c2-220">Чтобы упростить просмотр столбцов, с которыми вы работаете в определении строки, вы можете скорректировать ширину столбца, а также скрыть (минимизировать) или показать столбцы на панели просмотра.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="bb7c2-221">Внесенные изменения влияют только на внешний вид столбцов на экране.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="bb7c2-222">Они не влияют на форматирование столбцов в отчетах.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="bb7c2-223">Измените ширину столбца в панели просмотра</span><span class="sxs-lookup"><span data-stu-id="bb7c2-223">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="bb7c2-224">В конструкторе отчетов, раскройте определение строки, которое изменить.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-224">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-225">В меню **Формат**, выберите **Ширина столбца**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-225">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="bb7c2-226">В диалоговом окне **Ширина столбца** введите значение и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="bb7c2-227">Либо перетащите правую границу ячейки заголовка столбца, чтобы изменить ширину столбца.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="bb7c2-228">Скрыть столбцы в панели просмотра</span><span class="sxs-lookup"><span data-stu-id="bb7c2-228">Hide columns in the view pane</span></span>

1. <span data-ttu-id="bb7c2-229">В конструкторе отчетов, раскройте определение строки, которое изменить.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-229">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-230">Выберите столбец или столбцы, которые требуется свернуть.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-230">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="bb7c2-231">Щелкните правой кнопкой мыши и выберите **Скрыть**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="bb7c2-232">Покажите все скрытые столбцы в панели просмотра</span><span class="sxs-lookup"><span data-stu-id="bb7c2-232">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="bb7c2-233">В конструкторе отчетов, раскройте определение строки, которое изменить.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-233">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="bb7c2-234">Щелкните правой кнопкой мыши минимизированный столбец для отображения и щелкните **Показать**.</span><span class="sxs-lookup"><span data-stu-id="bb7c2-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="bb7c2-235">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bb7c2-235">Additional resources</span></span>

[<span data-ttu-id="bb7c2-236">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="bb7c2-236">Financial reporting</span></span>](financial-reporting-intro.md)
