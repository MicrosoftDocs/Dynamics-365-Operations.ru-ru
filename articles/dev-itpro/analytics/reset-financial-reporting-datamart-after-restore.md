---
title: "Сброс киоска данных финансовой отчетности"
description: "В этом разделе описывается сброс киоска данных финансовой отчетности."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: ru-ru
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="397c4-103">Сброс киоска данных финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="397c4-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="397c4-104">В этом разделе объясняется, как сбросить киоск данных финансовой отчетности для следующих версий:</span><span class="sxs-lookup"><span data-stu-id="397c4-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="397c4-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting, выпуск 7.2.6.0 и новее</span><span class="sxs-lookup"><span data-stu-id="397c4-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="397c4-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting, выпуск 7.0.10000.4 и новее</span><span class="sxs-lookup"><span data-stu-id="397c4-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="397c4-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (локальная версия)</span><span class="sxs-lookup"><span data-stu-id="397c4-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="397c4-108">Чтобы получить Finance and Operations Financial reporting выпуска 7.2.6.0 можно загрузить KB 4052514 по адресу <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="397c4-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="397c4-109">Сброс киоска данных финансовой отчетности для Finance and Operations Financial reporting выпуска 7.2.6.0 и новее</span><span class="sxs-lookup"><span data-stu-id="397c4-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="397c4-110">Сброс киоска данных финансовой отчетности из конструктора отчетов</span><span class="sxs-lookup"><span data-stu-id="397c4-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="397c4-111">Шаги в этом процессе поддерживаются для Finance and Operations Financial reporting выпуска 7.2.6.0 и новее.</span><span class="sxs-lookup"><span data-stu-id="397c4-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="397c4-112">В случае более раннего выпуска обратитесь за помощью в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="397c4-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="397c4-113">В определенных случаях может возникнуть необходимость сбросить киоск данных для финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="397c4-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="397c4-114">Можно выполнить эту задачу в клиенте конструктора отчетов.</span><span class="sxs-lookup"><span data-stu-id="397c4-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="397c4-115">Ниже приводятся некоторые сценарии, в которых может потребоваться сброс киоск данных:</span><span class="sxs-lookup"><span data-stu-id="397c4-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="397c4-116">База данных Finance and Operations была восстановлена, но база данных киоска данных не была восстановлена.</span><span class="sxs-lookup"><span data-stu-id="397c4-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="397c4-117">Вы видите неверные данные за период.</span><span class="sxs-lookup"><span data-stu-id="397c4-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="397c4-118">Службы поддержки дала инструкции сбросить киоск данных в процессе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="397c4-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="397c4-119">Сброс киоска данных должен выполняться только в течение времени, когда нагрузка на базу данных низкая.</span><span class="sxs-lookup"><span data-stu-id="397c4-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="397c4-120">Финансовая отчетность будут недоступна в процессе сброса.</span><span class="sxs-lookup"><span data-stu-id="397c4-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="397c4-121">Сброс киоска данных</span><span class="sxs-lookup"><span data-stu-id="397c4-121">Reset the data mart</span></span>

<span data-ttu-id="397c4-122">Чтобы сбросить киоск данных, в конструкторе отчетов в меню **Сервис** выберите пункт **Сброс киоска данных**.</span><span class="sxs-lookup"><span data-stu-id="397c4-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="397c4-123">Диалоговое окно, которое появляется, состоит из двух разделов: **Статистика** и **Сброс**.</span><span class="sxs-lookup"><span data-stu-id="397c4-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="397c4-124">[![Диалоговое окно сброса киоска данных](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="397c4-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="397c4-125">Попытки интеграции</span><span class="sxs-lookup"><span data-stu-id="397c4-125">Integration attempts</span></span>

<span data-ttu-id="397c4-126">Сетка **Попытки интеграции** показывает, сколько раз система пыталась интегрировать проводки.</span><span class="sxs-lookup"><span data-stu-id="397c4-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="397c4-127">Система продолжает попытки интеграции данных в течение некоторого количества дней, если первые несколько попыток были неудачными.</span><span class="sxs-lookup"><span data-stu-id="397c4-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="397c4-128">Вы будете знать, что необходимо произвести сброс киоска данных, если число попыток равно 8 или более, и если имеется много записей комбинации аналитик или проводок.</span><span class="sxs-lookup"><span data-stu-id="397c4-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="397c4-129">В этом случае данные не включаются в отчетность.</span><span class="sxs-lookup"><span data-stu-id="397c4-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="397c4-130">Статус данных</span><span class="sxs-lookup"><span data-stu-id="397c4-130">Data status</span></span>

<span data-ttu-id="397c4-131">Сетка **Статус данных** содержит моментальный снимок проводок, валютных курсов и значений аналитик в киоске данных.</span><span class="sxs-lookup"><span data-stu-id="397c4-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="397c4-132">Большое количество устаревших записей указывает, что было выполнено множество обновлений записей.</span><span class="sxs-lookup"><span data-stu-id="397c4-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="397c4-133">Это может привести к замедлению создания отчета.</span><span class="sxs-lookup"><span data-stu-id="397c4-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="397c4-134">Несопоставленные категории счетов ГК</span><span class="sxs-lookup"><span data-stu-id="397c4-134">Misaligned main account categories</span></span>

<span data-ttu-id="397c4-135">При использовании более раннего выпуска, чем Microsoft Dynamics 365 for Finance and Operations Financial reporting выпуска 7.2.1, может потребоваться сбросить киоск данных, если вы переименовали счета и перемещали счета между категориями счетов.</span><span class="sxs-lookup"><span data-stu-id="397c4-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="397c4-136">Эти действия могут вызвать нарушение согласования категорий счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="397c4-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="397c4-137">Поле **Несопоставленные категории счетов ГК** показывает, имеется ли такая проблема.</span><span class="sxs-lookup"><span data-stu-id="397c4-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="397c4-138">Сброс киоска данных в Finance and Operations Financial reporting выпуска 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="397c4-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="397c4-139">Для сброса киоска данных в Finance and Operations Financial reporting выпуска 7.2.6.0 и ранее в диалоговом окне **Сброс киоска данных** установите флажок **Сброс киоска данных**, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="397c4-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="397c4-140">Сброс киоска данных можно выполнять только во время запланированного перерыва.</span><span class="sxs-lookup"><span data-stu-id="397c4-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="397c4-141">[![Флажок сброса киоска данных](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="397c4-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="397c4-142">Сброс киоска данных и выбор причину в Microsoft Dynamics 365 for Finance and Operations Financial reporting выпуска 7.3.0</span><span class="sxs-lookup"><span data-stu-id="397c4-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="397c4-143">Если выясняется, что требуется сброс киоска данных, установите флажок **Сброс киоска данных**, затем выберите причину в поле **Причина**.</span><span class="sxs-lookup"><span data-stu-id="397c4-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="397c4-144">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="397c4-144">The following options are available:</span></span>

- <span data-ttu-id="397c4-145">**Отсутствующие или неправильные данные** — на основе статистики было определено, что данные могут отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="397c4-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="397c4-146">Прежде чем продолжить, рекомендуется провести работу со службой поддержки для определения основной причины.</span><span class="sxs-lookup"><span data-stu-id="397c4-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="397c4-147">**Восстановить базу данных** — база данных Finance and Operations была восстановлена, но база данных для киоска данных финансовой отчетности не была восстановлена.</span><span class="sxs-lookup"><span data-stu-id="397c4-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="397c4-148">**Прочее** — сброс киоска данных по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="397c4-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="397c4-149">Если вы считаете, что имеется проблема, обратитесь в службу поддержки для ее выявления.</span><span class="sxs-lookup"><span data-stu-id="397c4-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="397c4-150">Убедитесь, что интеграция всех существующих задач завершена, прежде чем выполнять эти действия.</span><span class="sxs-lookup"><span data-stu-id="397c4-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="397c4-151">Состояние интеграции можно посмотреть, выбрав **Сервис** &gt; **Статус интеграции**.</span><span class="sxs-lookup"><span data-stu-id="397c4-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="397c4-152">Очистить пользователей и компании</span><span class="sxs-lookup"><span data-stu-id="397c4-152">Clear users and companies</span></span>

<span data-ttu-id="397c4-153">Установите флажок **Очистить пользователей и компании**, если вы восстановили базу данных, но затем внесли изменения в пользователей или компании.</span><span class="sxs-lookup"><span data-stu-id="397c4-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="397c4-154">Устанавливать этот флажок требуется редко.</span><span class="sxs-lookup"><span data-stu-id="397c4-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="397c4-155">Когда вы будете готовы запустить процесс сброса, выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="397c4-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="397c4-156">Будет предложено подтвердить, что вы готовы начать процесс.</span><span class="sxs-lookup"><span data-stu-id="397c4-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="397c4-157">Обратите внимание, что Financial reporting не будут доступна во время сброса и начальной интеграции данных, которая выполняется впоследствии.</span><span class="sxs-lookup"><span data-stu-id="397c4-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="397c4-158">Если требуется просмотреть состояние интеграции, выберите **Сервис** &gt; **Статус интеграции** для просмотра времени выполнения последней интеграции и ее статуса.</span><span class="sxs-lookup"><span data-stu-id="397c4-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="397c4-159">[![Просмотр статуса интеграции](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="397c4-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="397c4-160">Сброс киоска данных финансовой отчетности для Finance and Operations Financial reporting выпуска 7.0.10000.4 и новее</span><span class="sxs-lookup"><span data-stu-id="397c4-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="397c4-161">Если вам когда-либо придется восстанавливать свою базу данных Finance and Operations из резервной копии или копировать базу данных из другой среды, необходимо выполнить действия, описанные в этой разделе, чтобы помочь гарантировать правильное использование киоском данных финансовой отчетности Financial reporting восстановленной базы данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397c4-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="397c4-162">Шаги в этом процессе поддерживаются для приложения Microsoft Dynamics AX версии 7.0.1 (май 2016) (сборка приложения 7.0.1265.23014 и сборка Financial reporting 7.0.10000.4) и позднее.</span><span class="sxs-lookup"><span data-stu-id="397c4-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="397c4-163">Если у вас более ранняя версия Finance and Operations, обратитесь в службу поддержки за помощью.</span><span class="sxs-lookup"><span data-stu-id="397c4-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="397c4-164">Экспорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="397c4-164">Export report definitions</span></span>

<span data-ttu-id="397c4-165">Во-первых, выполните следующие действия для экспорта моделей отчетов из конструктора отчетов.</span><span class="sxs-lookup"><span data-stu-id="397c4-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="397c4-166">В конструкторе отчетов выберите **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="397c4-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="397c4-167">Выберите группу строительных блоков, которую требуется экспортировать, затем выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="397c4-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="397c4-168">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="397c4-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="397c4-169">Выберите определения отчета для экспорта:</span><span class="sxs-lookup"><span data-stu-id="397c4-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="397c4-170">Чтобы экспортировать все определения отчетов и связанные с ними шаблоны, выберите **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="397c4-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="397c4-171">Чтобы экспортировать определенные отчеты, строки, столбцы, деревья или наборы аналитик, выберите соответствующую вкладку и выберите элементы для экспорта.</span><span class="sxs-lookup"><span data-stu-id="397c4-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="397c4-172">Нажмите и удерживайте клавишу CTRL, чтобы выбрать несколько элементов на вкладке. При выборе отчетов для экспорта выбираются соответствующие строки, столбцы, структуры и наборы аналитик.</span><span class="sxs-lookup"><span data-stu-id="397c4-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="397c4-173">Выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="397c4-173">Select **Export**.</span></span>
5. <span data-ttu-id="397c4-174">Введите имя файла и выберите безопасное место, где требуется сохранить экспортированные определения отчетов.</span><span class="sxs-lookup"><span data-stu-id="397c4-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="397c4-175">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="397c4-175">Select **Save**.</span></span>

<span data-ttu-id="397c4-176">Можно скопировать или отправить файл в надежное место.</span><span class="sxs-lookup"><span data-stu-id="397c4-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="397c4-177">Таким образом файл можно импортировать в другую среду позже.</span><span class="sxs-lookup"><span data-stu-id="397c4-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="397c4-178">Сведения об использовании учетной записи хранилища Microsoft Azure см. в разделе [Перенос данных с помощью служебной программы командной строки AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="397c4-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="397c4-179">Корпорация Майкрософт не предоставляет учетную запись хранилища в составе договора на Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397c4-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="397c4-180">Необходимо либо приобрести учетную запись хранилища, либо использовать учетную запись хранилища из отдельной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="397c4-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="397c4-181">Помните о поведении диска D в виртуальных машинах (VM) Azure.</span><span class="sxs-lookup"><span data-stu-id="397c4-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="397c4-182">Не хранит постоянно ваши экспортированные группы строительных блоков на диске D. Дополнительные сведения о временных дисках см. в разделе [Понимание временного диска на виртуальных машинах Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="397c4-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="397c4-183">Остановка служб</span><span class="sxs-lookup"><span data-stu-id="397c4-183">Stop services</span></span>

<span data-ttu-id="397c4-184">Следующие службы Microsoft Windows будут иметь открытые подключения к базе данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397c4-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="397c4-185">Поэтому необходимо использовать удаленный рабочий стол Microsoft, чтобы подключить все компьютеры в среде, и затем остановить эти службы с помощью services.msc.</span><span class="sxs-lookup"><span data-stu-id="397c4-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="397c4-186">Служба веб-публикаций (на всех компьютерах Application Object Servers [AOS])</span><span class="sxs-lookup"><span data-stu-id="397c4-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="397c4-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="397c4-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="397c4-188">Management Reporter 2012 Process Service (только на компьютерах Business intelligence [BI])</span><span class="sxs-lookup"><span data-stu-id="397c4-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="397c4-189">Сбросить</span><span class="sxs-lookup"><span data-stu-id="397c4-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="397c4-190">Загрузка последней версии пакета MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="397c4-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="397c4-191">Загрузите последнюю версию пакета MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="397c4-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="397c4-192">Сведения о том, как найти и загрузить правильную версию пакета обновления данных, см. в разделе [Загрузка последнего пакета развертывания обновления данных](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="397c4-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="397c4-193">Обновление не является обязательным для загрузки пакета MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="397c4-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="397c4-194">Таким образом, нужно просто выполнить действия, описанные в подразделе "Загрузка последнего пакета развертывания обновления данных" этого раздела.</span><span class="sxs-lookup"><span data-stu-id="397c4-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="397c4-195">Можно пропустить все остальные действия из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="397c4-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="397c4-196">Выполнение сценариев для базы данных Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="397c4-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="397c4-197">Запустите следующие сценарии для базы данных Finance and Operations (не для базы данных Financial reporting):</span><span class="sxs-lookup"><span data-stu-id="397c4-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="397c4-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="397c4-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="397c4-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="397c4-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="397c4-200">Эти сценарии помогает гарантировать правильность пользователей, ролей и параметров изменения отслеживания.</span><span class="sxs-lookup"><span data-stu-id="397c4-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="397c4-201">Выполнение команды Windows PowerShell для сброса базы данных</span><span class="sxs-lookup"><span data-stu-id="397c4-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="397c4-202">На компьютере с сервером AOS запустите Microsoft Windows PowerShell в качестве администратора и выполните следующие команды, чтобы сбросить интеграцию между Finance and Operations и Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="397c4-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="397c4-203">Ниже приводится объяснение параметров в команде **Reset-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="397c4-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="397c4-204">Допустимые значения для параметра **-Reason**: **SERVICING**, **BADDATA** и **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="397c4-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="397c4-205">Параметр **-ReasonDetail** является произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="397c4-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="397c4-206">Значения параметров Reason и ReasonDetail записываются в данных телеметрии/мониторинга среды.</span><span class="sxs-lookup"><span data-stu-id="397c4-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="397c4-207">После выполнения команд будет предложено ввести **Y** для подтверждения сброса базы данных.</span><span class="sxs-lookup"><span data-stu-id="397c4-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="397c4-208">Перезапуск служб</span><span class="sxs-lookup"><span data-stu-id="397c4-208">Restart services</span></span>

<span data-ttu-id="397c4-209">Используйте services.msc, чтобы перезапустить службы, остановленные ранее:</span><span class="sxs-lookup"><span data-stu-id="397c4-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="397c4-210">Служба веб-публикаций (на всех компьютерах AOS)</span><span class="sxs-lookup"><span data-stu-id="397c4-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="397c4-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="397c4-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="397c4-212">Management Reporter 2012 Process Service (только на компьютерах BI)</span><span class="sxs-lookup"><span data-stu-id="397c4-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="397c4-213">Импорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="397c4-213">Import report definitions</span></span>

<span data-ttu-id="397c4-214">Импортируйте макеты отчетов из конструктора отчетов, используя файл, созданный во время экспорта.</span><span class="sxs-lookup"><span data-stu-id="397c4-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="397c4-215">В конструкторе отчетов выберите **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="397c4-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="397c4-216">Выберите группу строительных блоков, которую требуется экспортировать, затем выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="397c4-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="397c4-217">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="397c4-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="397c4-218">Выберите строительный блок **По умолчанию**, затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="397c4-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="397c4-219">Выберите файл, содержащий экспортированные определения отчетов, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="397c4-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="397c4-220">В диалоговом окне **Импорт** выберите определения отчетов для импорта:</span><span class="sxs-lookup"><span data-stu-id="397c4-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="397c4-221">Чтобы импортировать все определения отчетов и связанные с ними шаблоны, выберите **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="397c4-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="397c4-222">Чтобы импортировать конкретные отчеты, строки, столбцы, деревья или наборы измерений, выберите отчеты, строки, столбцы, деревья или наборы измерений, которые необходимо импортировать, а затем нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="397c4-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="397c4-223">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="397c4-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="397c4-224">Сброс киоска данных финансовой отчетности Financial reporting для Finance and Operations (локальная версия)</span><span class="sxs-lookup"><span data-stu-id="397c4-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="397c4-225">Попросите всех пользователей выйти из конструктора отчетов и области финансовой отчетности в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397c4-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="397c4-226">Запустите следующий сценарий для базы данных финансовой отчетности (MRDB).</span><span class="sxs-lookup"><span data-stu-id="397c4-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="397c4-227">Выполните усечение или удалите все записи из таблицы FINANCIALREPORTS в базе данных Finance and Operations (AXDB).</span><span class="sxs-lookup"><span data-stu-id="397c4-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="397c4-228">Выполните усечение или удалите все записи из таблицы FINANCIALREPORTVERSION, если эта таблица имеется в базе данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397c4-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="397c4-229">Если таблица не существует в базе данных Finance and Operations, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="397c4-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="397c4-230">Запустите сценарий **ResetDatamart.sql** для базы данных финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="397c4-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="397c4-231">Этот сценарий отключает интеграцию киоска данных, удаляет все данные киоска данных, затем снова включает интеграцию киоска данных.</span><span class="sxs-lookup"><span data-stu-id="397c4-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="397c4-232">После сброса можно вручную проверить повторную загрузку данных, выполнив следующий запрос базы данных финансовых отчетов Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="397c4-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="397c4-233">Убедитесь, что все строки имеют значение **LastRunTime**, а параметр **StateType** имеет значение **5**.</span><span class="sxs-lookup"><span data-stu-id="397c4-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="397c4-234">Значение **5** параметра **StateType** означает, что данные были успешно перезагружены.</span><span class="sxs-lookup"><span data-stu-id="397c4-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="397c4-235">Значение **7** указывает на состояние сбоя.</span><span class="sxs-lookup"><span data-stu-id="397c4-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="397c4-236">В некоторых случаях карта организационной иерархии имеет это состояние при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="397c4-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="397c4-237">Тем не менее, это состояние ошибки должно быть автоматически разрешено.</span><span class="sxs-lookup"><span data-stu-id="397c4-237">However, the faulted state but should be automatically resolved.</span></span>

