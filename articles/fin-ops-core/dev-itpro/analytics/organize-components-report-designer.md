---
title: Организация компонентов отчета в конструкторе отчетов
description: В этой теме объясняется, как организовать существующие отчеты, строительные блоки и объекты в конструкторе отчетов.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cb3e09ad849b250ed3f1d7aec910b44d591cb88e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751640"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="87ffb-103">Организация компонентов отчета в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87ffb-104">После разработки строительных блоков и созданных отчетов рекомендуется организовать эти объекты для того, чтобы пользователям было проще их искать.</span><span class="sxs-lookup"><span data-stu-id="87ffb-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="87ffb-105">В этой статье объясняется, как организовать существующие отчеты, строительные блоки и объекты в конструкторе отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="87ffb-106">Вы можете переименовать папки, отчеты, строительные блоки и другие объекты в конструкторе отчетов, чтобы организовать свои файлы.</span><span class="sxs-lookup"><span data-stu-id="87ffb-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="87ffb-107">В зависимости от типа объекта, который вы переименовываете, вам может потребоваться обновить связи с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="87ffb-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="87ffb-108">Переименуйте папку или строительный блок в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="87ffb-109">В конструкторе отчетов можно переименовать папки, определения столбцов, строк и аналитических структур.</span><span class="sxs-lookup"><span data-stu-id="87ffb-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="87ffb-110">Переименование папки или шаблона в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="87ffb-111">Используйте панель переходов конструктора отчетов, чтобы найти нужную папку или объект.</span><span class="sxs-lookup"><span data-stu-id="87ffb-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="87ffb-112">Щелкните правой кнопкой мыши папку или объект и щелкните **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="87ffb-113">Поле **Имя** в области перехода становится доступным.</span><span class="sxs-lookup"><span data-stu-id="87ffb-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="87ffb-114">Напечатайте новое имя, и нажмите Ввод.</span><span class="sxs-lookup"><span data-stu-id="87ffb-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="87ffb-115">Если строительный блок — это определение строки, определение столбца или определение дерева отчетности, то вы должны обновить другие строительные блоки, которые связаны с ним.</span><span class="sxs-lookup"><span data-stu-id="87ffb-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="87ffb-116">Щелкните правой кнопкой мыши строительный блок, который вы переименовали на шаге 3, выберите **Ассоциации** и выберите элемент в списке, чтобы обновить его.</span><span class="sxs-lookup"><span data-stu-id="87ffb-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="87ffb-117">Повторите шаг 4, пока все связанные элементы не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="87ffb-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="87ffb-118">Создание и управление группами отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-118">Create and manage report groups</span></span>
<span data-ttu-id="87ffb-119">Вы можете собрать определения отчетов, чтобы произвести множественные отчеты в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="87ffb-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="87ffb-120">Чтобы создать, изменить, удалить и сгенерировать группы отчетов, вы должны иметь роль "Конструктор" или "Администратор".</span><span class="sxs-lookup"><span data-stu-id="87ffb-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="87ffb-121">Пользователи с ролью создателя могут создавать группы отчетов и изменять пользовательские настройки определений отчетов для групп отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="87ffb-122">Создание группы отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-122">Create a report group</span></span>

1. <span data-ttu-id="87ffb-123">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="87ffb-124">В меню **Файл** щелкните **Создать** &gt; **Определение группы отчетов**, чтобы открыть новую группу отчетов в окне средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="87ffb-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="87ffb-125">Либо нажмите кнопку **Группа отчетов** ![Группа отчетов](media/report-group.gif "Группа отчетов") на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="87ffb-126">Перейдите на вкладку **Группа отчетов**. Для того чтобы переопределить информацию об индивидуальных определениях отчетов для создания этого отчета, выберите флажок **Переопределить настройки компании, подробностей и даты из определений отдельного отчета**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="87ffb-127">Имя компании, уровень детализации, предварительные параметры и информация о дате заполняются автоматически, но вы можете вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="87ffb-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="87ffb-128">Чтобы создать несколько отчетов, в которых отображаются валюты отчетности, установите флажок **Включить все валюты отчетности**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="87ffb-129">Затем можно получить доступ к нескольким представлениям, нажав кнопку **Валюта** в средстве просмотра Интернета при просмотре отчета.</span><span class="sxs-lookup"><span data-stu-id="87ffb-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="87ffb-130">В поле **Отчеты в группе** щелкните **Добавить**, чтобы выбрать отчеты, которые требуется включить в группу отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="87ffb-131">Чтобы выбрать несколько отчетов, в диалоговом окне **Добавить** удерживайте клавишу CTRL, выбирая отчеты.</span><span class="sxs-lookup"><span data-stu-id="87ffb-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="87ffb-132">Закончив выбор отчетов, нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="87ffb-133">Щелкните **Файл** &gt; **Сохранить**, чтобы сохранить новую группу отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="87ffb-134">Изменить группу отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-134">Modify a report group</span></span>

1. <span data-ttu-id="87ffb-135">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="87ffb-136">Дважды щелкните группу отчетов, чтобы изменить ее.</span><span class="sxs-lookup"><span data-stu-id="87ffb-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="87ffb-137">На вкладке **Группа отчетов** внесите требуемые изменения.</span><span class="sxs-lookup"><span data-stu-id="87ffb-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="87ffb-138">В меню **Файл** щелкните **Сохранить**, чтобы сохранить измененную группу отчетов. Либо нажмите кнопку **Сохранить** ![Сохранить](media/save.gif "Сохранение") на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="87ffb-139">[ПРИМЕЧАНИЕ] Если вы запланировали создание отчетов через заданные интервалы, вы можете переопределить эти настройки и создать отчет немедленно.</span><span class="sxs-lookup"><span data-stu-id="87ffb-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="87ffb-140">Генерировать отчет группы отчета</span><span class="sxs-lookup"><span data-stu-id="87ffb-140">Generate a report group report</span></span>

1. <span data-ttu-id="87ffb-141">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="87ffb-142">Откройте группу отчетов для генерирования.</span><span class="sxs-lookup"><span data-stu-id="87ffb-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="87ffb-143">Нажмите кнопку **Создать отчет** ![Создать отчет](media/generate-report.gif "Создать отчет") для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="87ffb-144">Удаление группы отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-144">Delete a report group</span></span>

1. <span data-ttu-id="87ffb-145">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="87ffb-146">Щелкните правой кнопкой мыши группу отчетов для удаления и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="87ffb-147">В появившемся подтверждающем сообщении щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="87ffb-148">Элементы управления вкладки "Группа отчетов"</span><span class="sxs-lookup"><span data-stu-id="87ffb-148">Report Group tab controls</span></span>
<span data-ttu-id="87ffb-149">В следующей таблице описаны элементы управления на вкладке **Группа отчетов**.</span><span class="sxs-lookup"><span data-stu-id="87ffb-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="87ffb-150">Проверка</span><span class="sxs-lookup"><span data-stu-id="87ffb-150">Control</span></span></th>
<th><span data-ttu-id="87ffb-151">Описание</span><span class="sxs-lookup"><span data-stu-id="87ffb-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="87ffb-152">Перекрыть настройки компании, сведений и даты из индивидуальных определений отчетов</span><span class="sxs-lookup"><span data-stu-id="87ffb-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="87ffb-153">Выберите этот флажок, чтобы перекрыть индивидуальные определения отчета отчетов в этой группе отчетов только для генерирования этих отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-154">Название компании</span><span class="sxs-lookup"><span data-stu-id="87ffb-154">Company name</span></span></td>
<td><span data-ttu-id="87ffb-155">Выбор компании, которая будет использоваться в отчетах.</span><span class="sxs-lookup"><span data-stu-id="87ffb-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-156">Уровень детализации</span><span class="sxs-lookup"><span data-stu-id="87ffb-156">Detail level</span></span></td>
<td><span data-ttu-id="87ffb-157">Укажите уровень детализации отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="87ffb-158"><strong>Финансы</strong> — обобщенный сводный отчет.</span><span class="sxs-lookup"><span data-stu-id="87ffb-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="87ffb-159">Вы не можете детализировать до счетов и аналитик за исключением тех, которые добавлены с помощью дерева отчетности.</span><span class="sxs-lookup"><span data-stu-id="87ffb-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="87ffb-160"><strong>Финансовый и счет</strong> — отчет, содержащий сводку высокого уровня и сведения счета.</span><span class="sxs-lookup"><span data-stu-id="87ffb-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="87ffb-161"><strong>Финансовый, счет и проводка</strong> — отчет, содержащий сводку высокого уровня и сведения проводки.</span><span class="sxs-lookup"><span data-stu-id="87ffb-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-162">Промежуточный</span><span class="sxs-lookup"><span data-stu-id="87ffb-162">Provisional</span></span></td>
<td><span data-ttu-id="87ffb-163">Укажите типы действий отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="87ffb-164"><strong>Только разнесенные операции</strong> — включает только проводки и сальдо, которые были разнесены в финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="87ffb-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="87ffb-165"><strong>Разнесенные и неразнесенные операции</strong> — включает все проводки и сальдо, которые были введены и разнесены в финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="87ffb-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="87ffb-166"><strong>Только неразнесенные операции</strong> — включает только проводки, введенные в финансовых данных, но еще не разнесенные.</span><span class="sxs-lookup"><span data-stu-id="87ffb-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-167">Включить все валюты отчетности</span><span class="sxs-lookup"><span data-stu-id="87ffb-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="87ffb-168">Здесь перечислены все дополнительные валюты отчетности, настроенные в системе Microsoft Dynamics ERP.</span><span class="sxs-lookup"><span data-stu-id="87ffb-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="87ffb-169">Установите этот флажок, чтобы создать дополнительные отчеты в указанных валютах.</span><span class="sxs-lookup"><span data-stu-id="87ffb-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="87ffb-170">Чтобы просмотреть отчеты в веб-средстве просмотра, нажмите кнопку <strong>Валюта</strong> и выберите валюту.</span><span class="sxs-lookup"><span data-stu-id="87ffb-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-171">Информация о дате не сохраняется с определением отчета</span><span class="sxs-lookup"><span data-stu-id="87ffb-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="87ffb-172">Базовый период</span><span class="sxs-lookup"><span data-stu-id="87ffb-172">Base period</span></span></li>
<li><span data-ttu-id="87ffb-173">Базовый год</span><span class="sxs-lookup"><span data-stu-id="87ffb-173">Base year</span></span></li>
<li><span data-ttu-id="87ffb-174">Покрытый период</span><span class="sxs-lookup"><span data-stu-id="87ffb-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="87ffb-175">Только параметры базового периода по умолчанию сохраняются с определением отчета.</span><span class="sxs-lookup"><span data-stu-id="87ffb-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-176">Информация о дате сохраняется с определением отчета</span><span class="sxs-lookup"><span data-stu-id="87ffb-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="87ffb-177">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="87ffb-177">Report date</span></span></li>
<li><span data-ttu-id="87ffb-178">Базовый период по умолчанию</span><span class="sxs-lookup"><span data-stu-id="87ffb-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="87ffb-179">Отчеты в группе</span><span class="sxs-lookup"><span data-stu-id="87ffb-179">Reports in group</span></span></td>
<td><span data-ttu-id="87ffb-180">Добавьте, извлеките, и изменить порядок отчетов в группе отчетов.</span><span class="sxs-lookup"><span data-stu-id="87ffb-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="87ffb-181">Чтобы добавить определения отчетов к группе, дважды щелкните по группе для её открытия и нажмите кнопку <strong>Добавить</strong>.</span><span class="sxs-lookup"><span data-stu-id="87ffb-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="87ffb-182">Выберите отчеты, включаемые в группу, и нажмите кнопку <strong>ОК</strong>.</span><span class="sxs-lookup"><span data-stu-id="87ffb-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="87ffb-183">Чтобы убрать отчет из группы, выберите его и нажмите кнопку <strong>Удалить</strong>.</span><span class="sxs-lookup"><span data-stu-id="87ffb-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="87ffb-184">Чтобы изменить порядок, в котором создаются отчеты, выберите отчет в списке и щелкните <strong>Переместить вверх</strong> или <strong>Переместить вниз</strong>.</span><span class="sxs-lookup"><span data-stu-id="87ffb-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="87ffb-185">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87ffb-185">Additional resources</span></span>

[<span data-ttu-id="87ffb-186">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="87ffb-186">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]