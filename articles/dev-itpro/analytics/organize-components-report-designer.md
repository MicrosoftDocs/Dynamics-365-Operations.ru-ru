---
title: "Организация компонентов отчета в конструкторе отчетов"
description: "После разработки строительных блоков и созданных отчетов рекомендуется организовать эти объекты для того, чтобы пользователям было проще их искать. В этой статье объясняется, как организовать существующие отчеты, строительные блоки и объекты в конструкторе отчетов."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7207febc58dbab1df5551ae0f74ad74d9ced8e56
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="3c693-104">Организация компонентов отчета в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c693-105">После разработки строительных блоков и созданных отчетов рекомендуется организовать эти объекты для того, чтобы пользователям было проще их искать.</span><span class="sxs-lookup"><span data-stu-id="3c693-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="3c693-106">В этой статье объясняется, как организовать существующие отчеты, строительные блоки и объекты в конструкторе отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="3c693-107">Вы можете переименовать папки, отчеты, строительные блоки и другие объекты в конструкторе отчетов, чтобы организовать свои файлы.</span><span class="sxs-lookup"><span data-stu-id="3c693-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="3c693-108">В зависимости от типа объекта, который вы переименовываете, вам может потребоваться обновить связи с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="3c693-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3c693-109">Переименуйте папку или строительный блок в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="3c693-110">В конструкторе отчетов можно переименовать папки, определения отчета, определения строки, определения столбца и определения дерева отчетности.</span><span class="sxs-lookup"><span data-stu-id="3c693-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="3c693-111">**Примечание.** При переименовании строительного блока необходимо обновить все определения отчетности, использующие этот строительный блок.</span><span class="sxs-lookup"><span data-stu-id="3c693-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="3c693-112">В противном случае создать новый отчет невозможно.</span><span class="sxs-lookup"><span data-stu-id="3c693-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3c693-113">Переименуйте папку или строительный блок в конструкторе отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="3c693-114">В конструкторе отчетов, используйте Область перехода для того, чтобы найти папку или объект, которые переименовать.</span><span class="sxs-lookup"><span data-stu-id="3c693-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="3c693-115">Щелкните правой кнопкой мыши папку или объект и щелкните **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="3c693-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="3c693-116">Поле **Имя** в области перехода становится доступным.</span><span class="sxs-lookup"><span data-stu-id="3c693-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="3c693-117">Напечатайте новое имя, и нажмите Ввод.</span><span class="sxs-lookup"><span data-stu-id="3c693-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="3c693-118">Если строительный блок — это определение строки, определение столбца или определение дерева отчетности, то вы должны обновить другие строительные блоки, которые связаны с ним.</span><span class="sxs-lookup"><span data-stu-id="3c693-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="3c693-119">Щелкните правой кнопкой мыши строительный блок, который вы переименовали на шаге 3, выберите **Ассоциации** и выберите элемент в списке, чтобы обновить его.</span><span class="sxs-lookup"><span data-stu-id="3c693-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="3c693-120">Повторите шаг 4, пока все связанные элементы не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="3c693-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="3c693-121">Создание и управление группами отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-121">Create and manage report groups</span></span>
<span data-ttu-id="3c693-122">Вы можете собрать определения отчетов, чтобы произвести множественные отчеты в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="3c693-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="3c693-123">Чтобы создать, изменить, удалить и сгенерировать группы отчетов, вы должны иметь роль "Конструктор" или "Администратор".</span><span class="sxs-lookup"><span data-stu-id="3c693-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="3c693-124">Пользователи с ролью создателя могут создавать группы отчетов и изменять пользовательские настройки определений отчетов для групп отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="3c693-125">Создание группы отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-125">Create a report group</span></span>

1.  <span data-ttu-id="3c693-126">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="3c693-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="3c693-127">В меню **Файл** щелкните **Создать** &gt; **Определение группы отчетов**, чтобы открыть новую группу отчетов в окне средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="3c693-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="3c693-128">Либо нажмите кнопку **Группа отчетов** ![Группа отчетов](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Группа отчетов") на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3c693-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="3c693-129">Перейдите на вкладку **Группа отчетов**. Для того чтобы переопределить информацию об индивидуальных определениях отчетов для создания этого отчета, выберите флажок **Переопределить настройки компании, подробностей и даты из определений отдельного отчета**.</span><span class="sxs-lookup"><span data-stu-id="3c693-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="3c693-130">Имя компании, уровень детализации, предварительные параметры и информация о дате заполняются автоматически, но вы можете вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="3c693-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="3c693-131">Чтобы создать несколько отчетов, в которых отображаются валюты отчетности, установите флажок **Включить все валюты отчетности**.</span><span class="sxs-lookup"><span data-stu-id="3c693-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="3c693-132">Затем можно получить доступ к нескольким представлениям, нажав кнопку **Валюта** в средстве просмотра Интернета при просмотре отчета.</span><span class="sxs-lookup"><span data-stu-id="3c693-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="3c693-133">В поле **Отчеты в группе** щелкните **Добавить**, чтобы выбрать отчеты, которые требуется включить в группу отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="3c693-134">Чтобы выбрать несколько отчетов, в диалоговом окне **Добавить** удерживайте клавишу CTRL, выбирая отчеты.</span><span class="sxs-lookup"><span data-stu-id="3c693-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="3c693-135">Закончив выбор отчетов, нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c693-135">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="3c693-136">Щелкните **Файл** &gt; **Сохранить**, чтобы сохранить новую группу отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="3c693-137">Изменить группу отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-137">Modify a report group</span></span>

1.  <span data-ttu-id="3c693-138">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="3c693-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="3c693-139">Дважды щелкните группу отчетов, чтобы изменить ее.</span><span class="sxs-lookup"><span data-stu-id="3c693-139">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="3c693-140">На вкладке **Группа отчетов** внесите требуемые изменения.</span><span class="sxs-lookup"><span data-stu-id="3c693-140">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="3c693-141">В меню **Файл** щелкните **Сохранить**, чтобы сохранить измененную группу отчетов. Либо нажмите кнопку **Сохранить** ![Сохранить](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Сохранить") на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3c693-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="3c693-142">**Примечание.** Если вы запланировали создание отчетов через заданные интервалы, вы можете переопределить эти настройки и создать отчет немедленно.</span><span class="sxs-lookup"><span data-stu-id="3c693-142">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="3c693-143">Генерировать отчет группы отчета</span><span class="sxs-lookup"><span data-stu-id="3c693-143">Generate a report group report</span></span>

1.  <span data-ttu-id="3c693-144">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="3c693-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="3c693-145">Откройте группу отчетов для генерирования.</span><span class="sxs-lookup"><span data-stu-id="3c693-145">Open the report group to generate.</span></span>
3.  <span data-ttu-id="3c693-146">Нажмите кнопку **Создать отчет** ![Создать отчет](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Создать отчет") для создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="3c693-147">Удаление группы отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-147">Delete a report group</span></span>

1.  <span data-ttu-id="3c693-148">В конструкторе отчетов в области перехода щелкните **Группы отчетов**.</span><span class="sxs-lookup"><span data-stu-id="3c693-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="3c693-149">Щелкните правой кнопкой мыши группу отчетов для удаления и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="3c693-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="3c693-150">В появившемся подтверждающем сообщении щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="3c693-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="3c693-151">Элементы управления вкладки "Группа отчетов"</span><span class="sxs-lookup"><span data-stu-id="3c693-151">Report Group tab controls</span></span>
<span data-ttu-id="3c693-152">В следующей таблице описаны элементы управления на вкладке **Группа отчетов**.</span><span class="sxs-lookup"><span data-stu-id="3c693-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c693-153">Проверка</span><span class="sxs-lookup"><span data-stu-id="3c693-153">Control</span></span></th>
<th><span data-ttu-id="3c693-154">Описание</span><span class="sxs-lookup"><span data-stu-id="3c693-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c693-155">Перекрыть настройки компании, сведений и даты из индивидуальных определений отчетов</span><span class="sxs-lookup"><span data-stu-id="3c693-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="3c693-156">Выберите этот флажок, чтобы перекрыть индивидуальные определения отчета отчетов в этой группе отчетов только для генерирования этих отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c693-157">Название компании</span><span class="sxs-lookup"><span data-stu-id="3c693-157">Company name</span></span></td>
<td><span data-ttu-id="3c693-158">Выбор компании, которая будет использоваться в отчетах.</span><span class="sxs-lookup"><span data-stu-id="3c693-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c693-159">Уровень детализации</span><span class="sxs-lookup"><span data-stu-id="3c693-159">Detail level</span></span></td>
<td><span data-ttu-id="3c693-160">Укажите уровень детализации отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3c693-161"><strong>Финансы</strong> — обобщенный сводный отчет.</span><span class="sxs-lookup"><span data-stu-id="3c693-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="3c693-162">Вы не можете детализировать до счетов и аналитик за исключением тех, которые добавлены с помощью дерева отчетности.</span><span class="sxs-lookup"><span data-stu-id="3c693-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="3c693-163"><strong>Финансовый и счет</strong> — отчет, содержащий сводку высокого уровня и сведения счета.</span><span class="sxs-lookup"><span data-stu-id="3c693-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="3c693-164"><strong>Финансовый, счет и проводка</strong> — отчет, содержащий сводку высокого уровня и сведения проводки.</span><span class="sxs-lookup"><span data-stu-id="3c693-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c693-165">Промежуточный</span><span class="sxs-lookup"><span data-stu-id="3c693-165">Provisional</span></span></td>
<td><span data-ttu-id="3c693-166">Укажите типы действий отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3c693-167"><strong>Только разнесенные операции</strong> — включает только проводки и сальдо, которые были разнесены в финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="3c693-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="3c693-168"><strong>Разнесенные и неразнесенные операции</strong> — включает все проводки и сальдо, которые были введены и разнесены в финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="3c693-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="3c693-169"><strong>Только неразнесенные операции</strong> — включает только проводки, введенные в финансовых данных, но еще не разнесенные.</span><span class="sxs-lookup"><span data-stu-id="3c693-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c693-170">Включить все валюты отчетности</span><span class="sxs-lookup"><span data-stu-id="3c693-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="3c693-171">Здесь перечислены все дополнительные валюты отчетности, настроенные в системе Microsoft Dynamics ERP.</span><span class="sxs-lookup"><span data-stu-id="3c693-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="3c693-172">Установите этот флажок, чтобы создать дополнительные отчеты в указанных валютах.</span><span class="sxs-lookup"><span data-stu-id="3c693-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="3c693-173">Чтобы просмотреть отчеты в веб-средстве просмотра, нажмите кнопку <strong>Валюта</strong> и выберите валюту.</span><span class="sxs-lookup"><span data-stu-id="3c693-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c693-174">Информация о дате не сохраняется с определением отчета</span><span class="sxs-lookup"><span data-stu-id="3c693-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3c693-175">Базовый период</span><span class="sxs-lookup"><span data-stu-id="3c693-175">Base period</span></span></li>
<li><span data-ttu-id="3c693-176">Базовый год</span><span class="sxs-lookup"><span data-stu-id="3c693-176">Base year</span></span></li>
<li><span data-ttu-id="3c693-177">Покрытый период</span><span class="sxs-lookup"><span data-stu-id="3c693-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="3c693-178">Только параметры базового периода по умолчанию сохраняются с определением отчета.</span><span class="sxs-lookup"><span data-stu-id="3c693-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c693-179">Информация о дате сохраняется с определением отчета</span><span class="sxs-lookup"><span data-stu-id="3c693-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3c693-180">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="3c693-180">Report date</span></span></li>
<li><span data-ttu-id="3c693-181">Базовый период по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3c693-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c693-182">Отчеты в группе</span><span class="sxs-lookup"><span data-stu-id="3c693-182">Reports in group</span></span></td>
<td><span data-ttu-id="3c693-183">Добавьте, извлеките, и изменить порядок отчетов в группе отчетов.</span><span class="sxs-lookup"><span data-stu-id="3c693-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="3c693-184">Чтобы добавить определения отчетов к группе, дважды щелкните по группе для её открытия и нажмите кнопку <strong>Добавить</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c693-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="3c693-185">Выберите отчеты, включаемые в группу, и нажмите кнопку <strong>ОК</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c693-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="3c693-186">Чтобы убрать отчет из группы, выберите его и нажмите кнопку <strong>Удалить</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c693-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="3c693-187">Чтобы изменить порядок, в котором создаются отчеты, выберите отчет в списке и щелкните <strong>Переместить вверх</strong> или <strong>Переместить вниз</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c693-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="3c693-188">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c693-188">Additional resources</span></span>
--------

[<span data-ttu-id="3c693-189">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="3c693-189">Financial reporting</span></span>](financial-reporting-intro.md)




