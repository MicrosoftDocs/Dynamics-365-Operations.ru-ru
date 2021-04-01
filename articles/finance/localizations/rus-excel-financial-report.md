---
title: Настройка финансовых отчетов в Excel (Россия)
description: В этом разделе приводится пошаговое описание процесса создания конфигурации электронной отчетности (ER), которая содержит шаблон для создания финансового отчета в формате Excel.
author: Anasyash
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3e66e9999f2abae6400b62c64b9296d89fb57082
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240547"
---
# <a name="configure-financial-reports-in-excel-russia"></a><span data-ttu-id="bb483-103">Настройка финансовых отчетов в Excel (Россия)</span><span class="sxs-lookup"><span data-stu-id="bb483-103">Configure financial reports in Excel (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb483-104">В этом разделе поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую шаблон для создания финансового отчета в формате Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bb483-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating a financial report in Microsoft Excel format.</span></span>

<span data-ttu-id="bb483-105">Перед прочтением этой темы необходимо ознакомиться с разделом [Создание конфигураций электронной отчетности (ER)](../../dev-itpro/analytics/electronic-reporting-configuration.md?toc=/fin-and-ops/toc.json) и связанными разделами по электронной отчетности, посвященными созданию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bb483-105">Before you read this topic, you should review [Create Electronic reporting (ER) configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md?toc=/fin-and-ops/toc.json) and related electronic reporting topics about creating configurations.</span></span>

## <a name="set-up-a-financial-report"></a><span data-ttu-id="bb483-106">Настройка финансового отчета</span><span class="sxs-lookup"><span data-stu-id="bb483-106">Set up a financial report</span></span>

<span data-ttu-id="bb483-107">Настройте финансовый отчет, чтобы он имел список ячеек финансового отчета и правил расчета ячеек в финансовых отчетах.</span><span class="sxs-lookup"><span data-stu-id="bb483-107">Set up a financial report so that it has the list of financial report cells and rules for calculating financial reports cells.</span></span>

1. <span data-ttu-id="bb483-108">Отправьте настройки пакета управления данными.</span><span class="sxs-lookup"><span data-stu-id="bb483-108">Upload data management package settings.</span></span> <span data-ttu-id="bb483-109">В этом примере отправьте настройки пакета управления данными **RU Accounting reporting 5.07 (2016).zip**, как описано в разделе [Учет отчетности в электронном формате](rus-accounting-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="bb483-109">For this example, upload the **RU Accounting reporting 5.07 (2016).zip** data management package settings as described in [Accounting reporting in electronic format](rus-accounting-reporting.md).</span></span>
2. <span data-ttu-id="bb483-110">Выберите **Главная книга \> Настройка финансовых отчетов \> Финансовые отчеты**.</span><span class="sxs-lookup"><span data-stu-id="bb483-110">Go to **General ledger \> Financial reports setup \> Financial reports**.</span></span>
3. <span data-ttu-id="bb483-111">Выберите строку, которая имеет значение **Баланс** в столбце **Код отчета**.</span><span class="sxs-lookup"><span data-stu-id="bb483-111">Select the line that has the value **Баланс** in the **Report code** column.</span></span>
4. <span data-ttu-id="bb483-112">Выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="bb483-112">Select **Setup**.</span></span>
5. <span data-ttu-id="bb483-113">На странице **Настройка реквизитов** настройте правила расчета для ячейки отчета, как описано в разделе [Финансовая отчетность (Россия)](rus-financial-reports.md#set-up-calculation-rules-for-report-cells).</span><span class="sxs-lookup"><span data-stu-id="bb483-113">On the **Requisites setup** page, set up calculation rules for report cells, as described in [Financial reporting (Russia)](rus-financial-reports.md#set-up-calculation-rules-for-report-cells).</span></span>

## <a name="create-an-excel-template-for-the-financial-report"></a><span data-ttu-id="bb483-114">Создание шаблона Excel для финансового отчета</span><span class="sxs-lookup"><span data-stu-id="bb483-114">Create an Excel template for the financial report</span></span>

<span data-ttu-id="bb483-115">Создание шаблона Excel для вашего финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-115">Create an Excel template for your financial report.</span></span> <span data-ttu-id="bb483-116">Как минимум необходимо назначить имена всем ячейкам Excel, которые должны иметь значения в отчете, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="bb483-116">At a minimum, you should assign names to all the Excel cells that should have values on the report that is generated.</span></span>

<span data-ttu-id="bb483-117">Например, загрузите [пример шаблона Excel для балансового отчета в России](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="bb483-117">For an example, download the [Excel template example for a Russian balance sheet](https://docs.microsoft.com/dynamics/s-e/).</span></span>

## <a name="create-an-er-configuration-for-the-financial-report-in-excel-format"></a><span data-ttu-id="bb483-118">Создание конфигурации электронной отчетности для финансового отчета в формате Excel</span><span class="sxs-lookup"><span data-stu-id="bb483-118">Create an ER configuration for the financial report in Excel format</span></span>

<span data-ttu-id="bb483-119">Создайте формат конфигурации электронной отчетности, основанный на модели электронной отчетности **Модель финансовых отчетов**.</span><span class="sxs-lookup"><span data-stu-id="bb483-119">Create an ER configuration format that is based on the **Financial reports model** ER model.</span></span>

<span data-ttu-id="bb483-120">Перед выполнением этой процедуры см. раздел [Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML (ноябрь 2016 г.)](../../dev-itpro/analytics/tasks/er-design-reports-openxml-2016-11.md?toc=/fin-and-ops/toc.json) со сведениями о том, как настроить конфигурацию электронной отчетности, которая создает отчет в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="bb483-120">Before you complete this procedure, see [ER Design a configuration for generating reports in OPENXML format (November 2016)](../../dev-itpro/analytics/tasks/er-design-reports-openxml-2016-11.md?toc=/fin-and-ops/toc.json) for information about how to set up an ER configuration that generates a report in Excel format.</span></span>

1. <span data-ttu-id="bb483-121">Загрузите последнюю версию из перечисленных ниже конфигураций электронной отчетности:</span><span class="sxs-lookup"><span data-stu-id="bb483-121">Download the latest version of the following ER configurations:</span></span>

    - <span data-ttu-id="bb483-122">Модель финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="bb483-122">Financial reports model</span></span>
    - <span data-ttu-id="bb483-123">Сопоставление моделей финансовых отчетов (RU)</span><span class="sxs-lookup"><span data-stu-id="bb483-123">Financial reports model mapping (RU)</span></span>
    - <span data-ttu-id="bb483-124">Пример формата балансового отчета Excel (RU)</span><span class="sxs-lookup"><span data-stu-id="bb483-124">Balance sheet format Excel example (RU)</span></span>

    <span data-ttu-id="bb483-125">Инструкции см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="bb483-125">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

2. <span data-ttu-id="bb483-126">Перейдите в раздел **Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="bb483-126">Go to **Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="bb483-127">Выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="bb483-127">Select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="bb483-128">Создайте формат для финансового отчета в формате Excel:</span><span class="sxs-lookup"><span data-stu-id="bb483-128">Create a format for a financial report in Excel format:</span></span>

    1. <span data-ttu-id="bb483-129">На странице **Конфигурации** выберите конфигурацию электронной отчетности **Модель финансовых отчетов**.</span><span class="sxs-lookup"><span data-stu-id="bb483-129">On the **Configurations** page, select the **Financial reports model** ER configuration.</span></span>
    2. <span data-ttu-id="bb483-130">В области действий выберите **Создать конфигурацию \> Формат на основе модели данных модели финансовых отчетов**.</span><span class="sxs-lookup"><span data-stu-id="bb483-130">On the Action Pane, select **Create configuration \> Format based on data model Financial reports model**.</span></span>
    3. <span data-ttu-id="bb483-131">Введите имя.</span><span class="sxs-lookup"><span data-stu-id="bb483-131">Enter a name.</span></span>
    4. <span data-ttu-id="bb483-132">В поле **Тип формата** выберите **Excel**.</span><span class="sxs-lookup"><span data-stu-id="bb483-132">In the **Format type** field, select **Excel**.</span></span>
    5. <span data-ttu-id="bb483-133">В поле **Определение модели данных** введите **Финансовый отчет**.</span><span class="sxs-lookup"><span data-stu-id="bb483-133">In the **Data model definition** field, select **Financial report**.</span></span>
    6. <span data-ttu-id="bb483-134">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="bb483-134">Select **Create configuration**.</span></span>
    7. <span data-ttu-id="bb483-135">Выберите новую конфигурацию, затем на панели операций выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="bb483-135">Select the new configuration, and then, on the Action Pane, select **Designer**.</span></span>
    8. <span data-ttu-id="bb483-136">На панели операций откройте вкладку **Импорт** и выберите **Импорт из Excel**.</span><span class="sxs-lookup"><span data-stu-id="bb483-136">On the Action Pane, on the **Import** tab, select **Import from Excel**.</span></span>
    9. <span data-ttu-id="bb483-137">В диалоговом окне **Импорт из Excel** выберите **Добавить шаблон**, затем выберите файл Excel **Balance sheet.xls**.</span><span class="sxs-lookup"><span data-stu-id="bb483-137">In the **Import from Excel** dialog box, select **Add template**, and then select the **Balance sheet.xls** Excel file.</span></span>
    10. <span data-ttu-id="bb483-138">Задайте для параметра **Создать элемент формата листа Excel** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="bb483-138">Set the **Create Excel Sheet format element** option to **Yes**.</span></span>
    11. <span data-ttu-id="bb483-139">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bb483-139">Select **OK**.</span></span>
    12. <span data-ttu-id="bb483-140">Проверьте ячейки, которые создаются из имен в шаблоне Excel.</span><span class="sxs-lookup"><span data-stu-id="bb483-140">Review the cells that are created from the names in the Excel template.</span></span>

        ![Ячейки сопоставления формата](media/rus-format-designer-mapping.jpg)

    13. <span data-ttu-id="bb483-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb483-142">Close the page.</span></span>

5. <span data-ttu-id="bb483-143">Настройте формат электронной отчетности **Пример балансового отчета в формате Excel (RU)**:</span><span class="sxs-lookup"><span data-stu-id="bb483-143">Configure the **Balance sheet format Excel example (RU)** ER format:</span></span>

    1. <span data-ttu-id="bb483-144">На странице **Конфигурации** выберите конфигурацию электронной отчетности **Пример балансового отчета в формате Excel (RU)**, затем в области действий выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="bb483-144">On the **Configurations** page, select the **Balance sheet format Excel example (RU)** ER configuration, and then, on the Action Pane, select **Designer**.</span></span>
    2. <span data-ttu-id="bb483-145">Разверните элемент формата **Excel = "Балансовый отчет"**, затем элемент формата **Лист\<стр.1_2\>**.</span><span class="sxs-lookup"><span data-stu-id="bb483-145">Expand the **Excel = "Balance sheet"** format element and then the **Sheet\<стр.1_2\>** format element.</span></span> <span data-ttu-id="bb483-146">Просмотрите все ячейки, которые будут содержать данные на выходе для финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-146">Review all cells that will contain data in the output for the financial report.</span></span>
    3. <span data-ttu-id="bb483-147">На вкладке **Сопоставление** просмотрите элементы **Модель финансовых отчетов**, которые являются источниками для ячеек финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-147">On the **Mapping** tab, review the elements of the **Financial reports model** that are sources for financial report cells.</span></span>
    4. <span data-ttu-id="bb483-148">Проверьте ячейки от **ДД** до **PrevPrevYear** (**ДД**, **ММ**, **ГГГГ**, **Название компании** и так далее).</span><span class="sxs-lookup"><span data-stu-id="bb483-148">Review the cells from **DD** through **PrevPrevYear** (**DD**, **MM**, **YYYY**, **Company name**, and so on).</span></span> <span data-ttu-id="bb483-149">Убедитесь в том, что они сопоставлены с элементами модели из группы **Заголовок**, которая содержит различные сведения об организации и отчете.</span><span class="sxs-lookup"><span data-stu-id="bb483-149">Make sure that they are mapped to model elements from the **Header** group that contains various information about the organization and report.</span></span>

        > [!NOTE]
        > <span data-ttu-id="bb483-150">Если любая информация об организации в финансовом отчете не находится в области **Модель финансовых отчетов**, можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bb483-150">If any of the information about the organization on your financial report isn't in scope **Financial reports model**, you can follow these steps:</span></span>
        >
        > 1. <span data-ttu-id="bb483-151">Если отсутствующие данные являются внешними, создайте формат параметра пользовательского ввода.</span><span class="sxs-lookup"><span data-stu-id="bb483-151">If the missed data is external, create format User input parameter.</span></span>
        > 2. <span data-ttu-id="bb483-152">Создайте производную модель на основе модели **Модель финансовых отчетов** и добавьте новые элементы модели.</span><span class="sxs-lookup"><span data-stu-id="bb483-152">Create a derived model that is based on the **Financial reports model**, and add new model elements.</span></span> <span data-ttu-id="bb483-153">Затем создайте сопоставление производной модели на основе **Сопоставление моделей финансовых отчетов** и свяжите новые элементы модели с источниками данных Finance.</span><span class="sxs-lookup"><span data-stu-id="bb483-153">Then create a derived model mapping that is based on **Financial reports model mapping**, and bind new model elements to Finance data sources.</span></span>
        >
        > <span data-ttu-id="bb483-154">Дополнительные сведения о создании моделей данных электронной отчетности см. в разделе [Электронная отчетность — Разработка модели данных для конкретного домена](../../dev-itpro/analytics/tasks/er-design-domain-specific-data-model-2016-11.md?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="bb483-154">For more information about how to create ER data models, see [ER Design domain specific data model](../../dev-itpro/analytics/tasks/er-design-domain-specific-data-model-2016-11.md?toc=/fin-and-ops/toc.json).</span></span>
 
        <span data-ttu-id="bb483-155">Для получения дополнительных сведений о том, как сопоставить элементы модели данных с источниками данных, см. следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="bb483-155">For more information about how to map data model elements to data sources, see the following topics:</span></span>

        - [<span data-ttu-id="bb483-156">Определение сопоставлений моделей электронной отчетности и выбор источников данных для них</span><span class="sxs-lookup"><span data-stu-id="bb483-156">Define ER model mappings and select data sources for them</span></span>](../../dev-itpro/analytics/tasks/er-define-model-mapping-select-data-sources-2016-11.md?toc=/fin-and-ops/toc.json)
        - [<span data-ttu-id="bb483-157">Электронная отчетность Сопоставление модели данных с выбранными источникам данных</span><span class="sxs-lookup"><span data-stu-id="bb483-157">ER Map data model to selected data sources</span></span>](../../dev-itpro/analytics/tasks/er-map-data-model-selected-data-sources-2016-11.md?toc=/fin-and-ops/toc.json)

    5. <span data-ttu-id="bb483-158">Проверьте ячейки, в которые экспортируются значения финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-158">Review the cells that the financial report values are exported to.</span></span> <span data-ttu-id="bb483-159">Например, ячейки **АктивВнеОбАНематАктПояснения**, **АктивВнеОбАНематАктСумОтч**, **АктивВнеОбАНематАктСумПрдщ** и **АктивВнеОбАНематАктСумПрдшв** сопоставляются следующим расчетным полям: **Calculations.'\$Values'("\<Input parameter = Cell name\>").Value** или **Calculations.'\$Values'("\<Input parameter = Cell code\>").Text**.</span><span class="sxs-lookup"><span data-stu-id="bb483-159">For example, the **АктивВнеОбАНематАктПояснения**, **АктивВнеОбАНематАктСумОтч**, **АктивВнеОбАНематАктСумПрдщ**, and **АктивВнеОбАНематАктСумПрдшв** cells are mapped to the following calculated field: **Calculations.'\$Values'("\<Input parameter = Cell name\>").Value** or **Calculations.'\$Values'("\<Input parameter = Cell code\>").Text**.</span></span>

        <span data-ttu-id="bb483-160">Вычисляемое поле **Calculations.'\$Values'** содержит значение ячейки финансового отчета с кодом, равным значению "Входной параметр".</span><span class="sxs-lookup"><span data-stu-id="bb483-160">The **Calculations.'\$Values'** calculated field contains the value of the financial report cell that has a code that equals the "Input parameter."</span></span>

        <span data-ttu-id="bb483-161">Дополнительные сведения о модели финансовых отчетов см. в разделе [Настройка электронной отчетности для использования результатов расчетов финансового отчета](rus-financial-reports.md#configure-er-to-use-the-results-of-financial-report-calculations).</span><span class="sxs-lookup"><span data-stu-id="bb483-161">For more information about the Financial reports model, see [Configure ER to use the results of financial report calculations](rus-financial-reports.md#configure-er-to-use-the-results-of-financial-report-calculations).</span></span>

6. <span data-ttu-id="bb483-162">Свяжите рассчитанные значения ячеек финансового отчета с элементами ячеек формата электронной отчетности:</span><span class="sxs-lookup"><span data-stu-id="bb483-162">Bind the calculated values of financial report cells to elements of the ER format cells:</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb483-163">В текущем примере элементы уже связаны в формат.</span><span class="sxs-lookup"><span data-stu-id="bb483-163">In the current example, elements are already bound in the format.</span></span> <span data-ttu-id="bb483-164">Чтобы выполнить шаги в этом примере, необходимо сначала отменить привязку элементов.</span><span class="sxs-lookup"><span data-stu-id="bb483-164">To complete the steps in the example, you must first unbind the elements.</span></span>
    > 
    > <span data-ttu-id="bb483-165">Выберите ячейку формата электронной отчетности **АктивВнеОбАНематАктПояснения**, затем выберите **Удалить привязку**.</span><span class="sxs-lookup"><span data-stu-id="bb483-165">Select the **АктивВнеОбАНематАктПояснения** ER format cell, and then select **Unbind**.</span></span> 
    > <span data-ttu-id="bb483-166">Повторите это для следующих трех ячеек формата электронной отчетности: **АктивВнеОбАНематАктСумОтч**, **АктивВнеОбАНематАктСумПрдщ** и **АктивВнеОбАНематАктСумПрдшв**.</span><span class="sxs-lookup"><span data-stu-id="bb483-166">Repeat this for the following three ER format cells: **АктивВнеОбАНематАктСумОтч**, **АктивВнеОбАНематАктСумПрдщ**, and **АктивВнеОбАНематАктСумПрдшв**.</span></span> 
    > <span data-ttu-id="bb483-167">Вам не потребуется делать это для новых отчетов.</span><span class="sxs-lookup"><span data-stu-id="bb483-167">You won't need to do this for your new reports.</span></span> 
    
    1. <span data-ttu-id="bb483-168">На вкладке **Сопоставление** разверните контейнер **Вычисления**, разверните вычисляемое поле **\$Значения** и выберите элемент **Текст**.</span><span class="sxs-lookup"><span data-stu-id="bb483-168">On the **Mapping** tab, expand the **Calculations** container, expand the **\$Values** calculated field, and select the **Text** element.</span></span>
    2. <span data-ttu-id="bb483-169">В списке ячеек формата Excel выберите ячейку **АктивВнеОбАНематАктПояснения**, затем выберите **Привязать**.</span><span class="sxs-lookup"><span data-stu-id="bb483-169">In the list of Excel format cells, select the **АктивВнеОбАНематАктПояснения** cell, and then select **Bind**.</span></span>

        ![Текстовая строка сопоставления формата](media/rus-format-designer-mapping-text-string.jpg)

    3. <span data-ttu-id="bb483-171">На вкладке **Сопоставление** выберите элемент **Значение**.</span><span class="sxs-lookup"><span data-stu-id="bb483-171">On the **Mapping** tab, select the **Value** element.</span></span>
    4. <span data-ttu-id="bb483-172">В списке ячеек формата Excel выберите ячейку **АктивВнеОбАНематАктСумОтч**, затем выберите **Привязать**.</span><span class="sxs-lookup"><span data-stu-id="bb483-172">In the list of Excel format cells, select the **АктивВнеОбАНематАктСумОтч** cell, and then select **Bind**.</span></span>
    5. <span data-ttu-id="bb483-173">Повторите предыдущие два шага для ячеек Excel **АктивВнеОбАНематАктСумПрдщ** и **АктивВнеОбАНематАктСумПрдшв**.</span><span class="sxs-lookup"><span data-stu-id="bb483-173">Repeat the previous two steps for **АктивВнеОбАНематАктСумПрдщ**, and **АктивВнеОбАНематАктСумПрдшв** Excel cells.</span></span>
    

## <a name="run-the-financial-report-format"></a><span data-ttu-id="bb483-174">Выполнение формат финансового отчета</span><span class="sxs-lookup"><span data-stu-id="bb483-174">Run the financial report format</span></span>

<span data-ttu-id="bb483-175">Можно настроить функцию электронных сообщений для выполнения любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="bb483-175">You can configure the Electronic messages feature to run any ER configuration.</span></span> <span data-ttu-id="bb483-176">Дополнительные сведения см. в разделе [Настройка электронных сообщений для создания финансового отчета и сохранения результатов](rus-financial-reports.md#configure-electronic-messages-to-generate-the-financial-report-and-store-the-results).</span><span class="sxs-lookup"><span data-stu-id="bb483-176">For more information, see [Configure electronic messages to generate the financial report and store the results](rus-financial-reports.md#configure-electronic-messages-to-generate-the-financial-report-and-store-the-results).</span></span>

<span data-ttu-id="bb483-177">Для запуска формата электронной отчетности, который основан на модели **Модель финансовых отчетов**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb483-177">To run the ER format that is based on the **Financial reports model**, follow these steps.</span></span>

1. <span data-ttu-id="bb483-178">Выберите **Главная книга \> Запросы и отчеты \> Финансовые отчеты (Россия)**.</span><span class="sxs-lookup"><span data-stu-id="bb483-178">Go to **General ledger \> Inquiries and reports \> Financial reports (Russia)**.</span></span>
2. <span data-ttu-id="bb483-179">В диалоговом окне **Финансовые отчеты (Россия)** в поле **Сопоставление формата** выберите формат электронной отчетности, который должен запускаться.</span><span class="sxs-lookup"><span data-stu-id="bb483-179">In the **Financial reports (Russia)** dialog box, in the **Format mapping** field, select the ER format that should be run.</span></span> <span data-ttu-id="bb483-180">Например, выберите **Пример формата балансового отчета Excel (RU)**.</span><span class="sxs-lookup"><span data-stu-id="bb483-180">For example, select **Balance sheet format Excel example (RU)**.</span></span>
3. <span data-ttu-id="bb483-181">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bb483-181">Select **OK**.</span></span>
4. <span data-ttu-id="bb483-182">В диалоговом окне **Параметры электронного отчета** определите параметры отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-182">In the **Electronic report parameters** dialog box, define the report parameters.</span></span>

    | <span data-ttu-id="bb483-183">Поле</span><span class="sxs-lookup"><span data-stu-id="bb483-183">Field</span></span>                                                            | <span data-ttu-id="bb483-184">Описание</span><span class="sxs-lookup"><span data-stu-id="bb483-184">Description</span></span> |
    |------------------------------------------------------------------|-------------|
    | <span data-ttu-id="bb483-185">Имя подписавшего, отчество подписавшего, фамилия подписавшего</span><span class="sxs-lookup"><span data-stu-id="bb483-185">Signatory first name, Signatory middle name, Signatory last name</span></span> | <span data-ttu-id="bb483-186">Введите полное имя подписавшего.</span><span class="sxs-lookup"><span data-stu-id="bb483-186">Enter the full name of the signatory.</span></span> |
    | <span data-ttu-id="bb483-187">До даты</span><span class="sxs-lookup"><span data-stu-id="bb483-187">To date</span></span>                                                          | <span data-ttu-id="bb483-188">Введите базовую дату финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-188">Enter the base date of the financial report.</span></span> |
    | <span data-ttu-id="bb483-189">Дата утверждения</span><span class="sxs-lookup"><span data-stu-id="bb483-189">Approval date</span></span>                                                    | <span data-ttu-id="bb483-190">Введите дату утверждения финансового отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-190">Enter the approval date of the financial report.</span></span> |
    | <span data-ttu-id="bb483-191">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="bb483-191">Reporting date</span></span>                                                   | <span data-ttu-id="bb483-192">Введите дату отчетности для корректирующего отчета.</span><span class="sxs-lookup"><span data-stu-id="bb483-192">Enter the reporting date for the corrective report.</span></span> |
    | <span data-ttu-id="bb483-193">ОКВЭД</span><span class="sxs-lookup"><span data-stu-id="bb483-193">Economic activity type code</span></span>                                      | <span data-ttu-id="bb483-194">Введите код типа хозяйственной деятельности ("ОКВЭД").</span><span class="sxs-lookup"><span data-stu-id="bb483-194">Enter the economic activity type code ("ОКВЭД").</span></span> |
    | <span data-ttu-id="bb483-195">Код формы организации</span><span class="sxs-lookup"><span data-stu-id="bb483-195">Organizational form code</span></span>                                         | <span data-ttu-id="bb483-196">Введите код организационной формы ("ОКОПФ").</span><span class="sxs-lookup"><span data-stu-id="bb483-196">Enter the organizational form code ("ОКОПФ").</span></span> |
    | <span data-ttu-id="bb483-197">Код формы собственности</span><span class="sxs-lookup"><span data-stu-id="bb483-197">Ownership form code</span></span>                                              | <span data-ttu-id="bb483-198">Введите код формы собственности ("ОКФС").</span><span class="sxs-lookup"><span data-stu-id="bb483-198">Enter the ownership form code ("ОКФС").</span></span> |
    | <span data-ttu-id="bb483-199">Отчет</span><span class="sxs-lookup"><span data-stu-id="bb483-199">Report</span></span>                                                           | <span data-ttu-id="bb483-200">Выберите финансовый отчет, который должен быть рассчитан.</span><span class="sxs-lookup"><span data-stu-id="bb483-200">Select the financial report that should be calculated.</span></span> <span data-ttu-id="bb483-201">В этом примере выберите **Баланс**.</span><span class="sxs-lookup"><span data-stu-id="bb483-201">For this example, select **Баланс**.</span></span> |

5. <span data-ttu-id="bb483-202">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bb483-202">Select **OK**.</span></span>
6. <span data-ttu-id="bb483-203">Просмотрите созданный отчет Excel.</span><span class="sxs-lookup"><span data-stu-id="bb483-203">Review the Excel report that is generated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]