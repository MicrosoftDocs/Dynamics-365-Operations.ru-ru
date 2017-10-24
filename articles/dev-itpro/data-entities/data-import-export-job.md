---
title: "Задания импорта и экспорта данных"
description: "Для создания заданий импорта и экспорта данных и управления ими служит рабочая область \"Управление данными\"."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c788b018f621144755cc0b4ee4b55cb633cd81be
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="data-import-and-export-jobs"></a><span data-ttu-id="4ee72-103">Задания импорта и экспорта данных</span><span class="sxs-lookup"><span data-stu-id="4ee72-103">Data import and export jobs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ee72-104">Для создания заданий импорта и экспорта данных и управления ими в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition служит рабочая область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-104">To create and manage data import and export jobs in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you use the **Data management** workspace.</span></span> <span data-ttu-id="4ee72-105">По умолчанию процесс импорта и экспорта данных создает промежуточную таблицу для каждого объекта в целевой базе данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-105">By default, the data import and export process creates a staging table for each entity in the target database.</span></span> <span data-ttu-id="4ee72-106">Промежуточные таблицы позволяют проверить, очистить или преобразовать данные перед перемещением.</span><span class="sxs-lookup"><span data-stu-id="4ee72-106">Staging tables let you verify, clean up, or convert data before you move it.</span></span>

## <a name="data-importexport-process"></a><span data-ttu-id="4ee72-107">Процесс импорта/экспорта данных</span><span class="sxs-lookup"><span data-stu-id="4ee72-107">Data import/export process</span></span>
<span data-ttu-id="4ee72-108">Ниже приведены шаги, необходимые для импорта или экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-108">Here are the steps to import or export data.</span></span>

1. <span data-ttu-id="4ee72-109">Создание задания импорта или экспорта, что предполагает выполнение следующих задач:</span><span class="sxs-lookup"><span data-stu-id="4ee72-109">Create an import or export job where you complete the following tasks:</span></span>

    - <span data-ttu-id="4ee72-110">Определение категории проекта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-110">Define the project category.</span></span>
    - <span data-ttu-id="4ee72-111">Определение объектов для импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-111">Identify the entities to import or export.</span></span>
    - <span data-ttu-id="4ee72-112">Определение формата данных для задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-112">Set the data format for the job.</span></span>
    - <span data-ttu-id="4ee72-113">Определение последовательности объектов, чтобы они обрабатывались в виде логических групп и в порядке, которые имеет какой-либо смысл.</span><span class="sxs-lookup"><span data-stu-id="4ee72-113">Sequence the entities, so that they are processed in logical groups and in an order that makes sense.</span></span>
    - <span data-ttu-id="4ee72-114">Определение того, следует ли использовать промежуточные таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ee72-114">Determine whether to use staging tables.</span></span>

2. <span data-ttu-id="4ee72-115">Проверка правильности сопоставления исходных данных и целевых данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-115">Validate that the source data and target data are mapped correctly.</span></span>
3. <span data-ttu-id="4ee72-116">Проверка параметров безопасности для задания импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-116">Verify the security for your import or export job.</span></span>
4. <span data-ttu-id="4ee72-117">Запуск задания импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-117">Run the import or export job.</span></span>
5. <span data-ttu-id="4ee72-118">Проверка правильности выполнения задания путем просмотра истории задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-118">Validate that the job ran as expected by reviewing the job history.</span></span>
6. <span data-ttu-id="4ee72-119">Очистка промежуточных таблиц.</span><span class="sxs-lookup"><span data-stu-id="4ee72-119">Clean up the staging tables.</span></span>

<span data-ttu-id="4ee72-120">В остальных разделах этой темы приведены дополнительные сведения о каждом шаге процесса.</span><span class="sxs-lookup"><span data-stu-id="4ee72-120">The remaining sections of this topic provide more details about each step of the process.</span></span>

## <a name="create-an-import-or-export-job"></a><span data-ttu-id="4ee72-121">Создание задания импорта или экспорта</span><span class="sxs-lookup"><span data-stu-id="4ee72-121">Create an import or export job</span></span>
<span data-ttu-id="4ee72-122">Задание импорта или экспорта данных можно запустить один раз или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="4ee72-122">A data import or export job can be run one time or many times.</span></span>

### <a name="define-the-project-category"></a><span data-ttu-id="4ee72-123">Определение категории проекта</span><span class="sxs-lookup"><span data-stu-id="4ee72-123">Define the project category</span></span>
<span data-ttu-id="4ee72-124">Рекомендуем подойти к выбору категории проекта для задания импорта или экспорта со всей тщательностью.</span><span class="sxs-lookup"><span data-stu-id="4ee72-124">We recommend that you take the time to select an appropriate project category for your import or export job.</span></span> <span data-ttu-id="4ee72-125">Категории проекта помогают управлять связанными заданиями.</span><span class="sxs-lookup"><span data-stu-id="4ee72-125">Project categories can help you manage related jobs.</span></span>

### <a name="identify-the-entities-to-import-or-export"></a><span data-ttu-id="4ee72-126">Определение объектов для импорта или экспорта</span><span class="sxs-lookup"><span data-stu-id="4ee72-126">Identify the entities to import or export</span></span>
<span data-ttu-id="4ee72-127">Можно добавить в задание импорта или экспорта конкретные объекты или выбрать шаблон для применения.</span><span class="sxs-lookup"><span data-stu-id="4ee72-127">You can add specific entities to an import or export job or select a template to apply.</span></span> <span data-ttu-id="4ee72-128">Шаблоны заполняют задание списком объектов.</span><span class="sxs-lookup"><span data-stu-id="4ee72-128">Templates fill a job with a list of entities.</span></span> <span data-ttu-id="4ee72-129">Действие **Применить шаблон** становится доступным после присвоения заданию имени и сохранения задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-129">The **Apply template** option is available after you give the job a name and save the job.</span></span>

### <a name="set-the-data-format-for-the-job"></a><span data-ttu-id="4ee72-130">Определение формата данных для задания</span><span class="sxs-lookup"><span data-stu-id="4ee72-130">Set the data format for the job</span></span>
<span data-ttu-id="4ee72-131">При выборе объекта необходимо выбрать формат данных, которые будут экспортированы или импортированы.</span><span class="sxs-lookup"><span data-stu-id="4ee72-131">When you select an entity, you must select the format of the data that will be exported or imported.</span></span> <span data-ttu-id="4ee72-132">Форматы определяются с помощью плитки **Настройка источников данных**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-132">You define formats by using the **Data sources setup** tile.</span></span> <span data-ttu-id="4ee72-133">Многие организации начинают с форматов, которые входят в набор демонстрационных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4ee72-133">Many organizations start from the formats that are included by default in the demo data set.</span></span> <span data-ttu-id="4ee72-134">Ниже приведен список некоторых из этих форматов:</span><span class="sxs-lookup"><span data-stu-id="4ee72-134">Here is a list of some of these formats:</span></span>

- <span data-ttu-id="4ee72-135">AX (для данных, которые должны импортироваться или экспортироваться в том же формате, который используется для Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition)</span><span class="sxs-lookup"><span data-stu-id="4ee72-135">AX (for data that must be imported or exported in the same format that is used for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition)</span></span>
- <span data-ttu-id="4ee72-136">ColonSeparated</span><span class="sxs-lookup"><span data-stu-id="4ee72-136">ColonSeparated</span></span>
- <span data-ttu-id="4ee72-137">Значения, разд. запятой</span><span class="sxs-lookup"><span data-stu-id="4ee72-137">CSV</span></span>
- <span data-ttu-id="4ee72-138">Excel</span><span class="sxs-lookup"><span data-stu-id="4ee72-138">Excel</span></span>
- <span data-ttu-id="4ee72-139">Пакет</span><span class="sxs-lookup"><span data-stu-id="4ee72-139">Package</span></span>

### <a name="sequence-the-entities"></a><span data-ttu-id="4ee72-140">Определение последовательности объектов</span><span class="sxs-lookup"><span data-stu-id="4ee72-140">Sequence the entities</span></span>
<span data-ttu-id="4ee72-141">Задать последовательность объектов можно в шаблоне данных или в заданиях импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-141">Entities can be sequenced in a data template, or in import and export jobs.</span></span> <span data-ttu-id="4ee72-142">При запуске задания, которое содержит несколько информационных объектов, необходимо убедиться, что информационные объекты следуют в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="4ee72-142">When you run a job that contains more than one data entity, you must make sure that the data entities are correctly sequenced.</span></span> <span data-ttu-id="4ee72-143">Последовательность объектов задается главным образом для учета всех функциональных зависимостей между объектами.</span><span class="sxs-lookup"><span data-stu-id="4ee72-143">You sequence entities primarily so that you can address any functional dependencies among entities.</span></span> <span data-ttu-id="4ee72-144">Если объекты не имеют никаких функциональных зависимостей, их можно импортировать или экспортировать параллельно.</span><span class="sxs-lookup"><span data-stu-id="4ee72-144">If entities don’t have any functional dependencies, they can be scheduled for parallel import or export.</span></span>

#### <a name="execution-units-levels-and-sequences"></a><span data-ttu-id="4ee72-145">Единицы выполнения, уровни и порядковые номера</span><span class="sxs-lookup"><span data-stu-id="4ee72-145">Execution units, levels, and sequences</span></span>
<span data-ttu-id="4ee72-146">Единица выполнения, уровень в единице выполнения и порядковый номер объекта помогают управлять порядком, в котором экспортируются или импортируются данные.</span><span class="sxs-lookup"><span data-stu-id="4ee72-146">The execution unit, level in the execution unit, and sequence of an entity help control the order that the data is exported or imported in.</span></span>

- <span data-ttu-id="4ee72-147">Объекты в различных единицах выполнения обрабатываются параллельно.</span><span class="sxs-lookup"><span data-stu-id="4ee72-147">Entities in different execution units are processed in parallel.</span></span>
- <span data-ttu-id="4ee72-148">В каждой единице выполнения объекты обрабатываются параллельно, если они имеют один и тот же уровень.</span><span class="sxs-lookup"><span data-stu-id="4ee72-148">In each execution unit, entities are processed in parallel if they have the same level.</span></span>
- <span data-ttu-id="4ee72-149">На каждом уровне объекты обрабатываются в соответствии с их порядковым номером на данном уровне.</span><span class="sxs-lookup"><span data-stu-id="4ee72-149">In each level, entities are processed according to their sequence number in that level.</span></span>
- <span data-ttu-id="4ee72-150">После завершения обработки одного уровня обрабатывается следующий уровень.</span><span class="sxs-lookup"><span data-stu-id="4ee72-150">After one level has been processed, the next level is processed.</span></span>

#### <a name="resequencing"></a><span data-ttu-id="4ee72-151">Изменение последовательности</span><span class="sxs-lookup"><span data-stu-id="4ee72-151">Resequencing</span></span>
<span data-ttu-id="4ee72-152">Изменить последовательность объектом может понадобиться в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="4ee72-152">You might want to resequence your entities in the following situations:</span></span>

- <span data-ttu-id="4ee72-153">Если для всех ваших изменений используется только одно задание, вы можете использовать команды изменения последовательности для оптимизации времени выполнения всего задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-153">If only one data job is used for all your changes, you can use resequencing options to optimize the execution time for the full job.</span></span> <span data-ttu-id="4ee72-154">В этих случаях можно использовать единицу выполнения для представления модуля, уровень для представления функциональной области в модуле, а порядковый номер для представления объекта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-154">In these cases, you can use the execution unit to represent the module, the level to represent the feature area in the module, and the sequence to represent the entity.</span></span> <span data-ttu-id="4ee72-155">При таком подходе можно работать между модулями в параллельном режиме, но в пределах модуля все равно работать в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="4ee72-155">By using this approach, you can work across modules in parallel, but you can still work in sequence in a module.</span></span> <span data-ttu-id="4ee72-156">Чтобы гарантировать успешное выполнение параллельных операций, необходимо учитывать все зависимости.</span><span class="sxs-lookup"><span data-stu-id="4ee72-156">To help guarantee that parallel operations succeed, you must consider all dependencies.</span></span>
- <span data-ttu-id="4ee72-157">Если используется несколько заданий данных (например, по одному заданию для каждого модуля), задание последовательности может влиять на уровень и порядковый номер для оптимального выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ee72-157">If multiple data jobs are used (for example, one job for each module), you can use sequencing to affect the level and sequence of entities for optimal execution.</span></span>
- <span data-ttu-id="4ee72-158">Если зависимости отсутствуют вообще, вы можете задать последовательность объектов в различных единицах выполнения для максимальной оптимизации.</span><span class="sxs-lookup"><span data-stu-id="4ee72-158">If there are no dependencies at all, you can sequence entities at different execution units for maximum optimization.</span></span>

<span data-ttu-id="4ee72-159">Меню **Изменение последовательности** доступно, когда выбрано несколько объектов.</span><span class="sxs-lookup"><span data-stu-id="4ee72-159">The **Resequencing** menu is available when multiple entities are selected.</span></span> <span data-ttu-id="4ee72-160">Изменять последовательность можно по единицам измерения, уровням или порядковым номерам.</span><span class="sxs-lookup"><span data-stu-id="4ee72-160">You can resequence based on execution unit, level, or sequence options.</span></span> <span data-ttu-id="4ee72-161">Можно задать приращение для изменения последовательности выбранных объектов.</span><span class="sxs-lookup"><span data-stu-id="4ee72-161">You can set an increment to resequence the entities that have been selected.</span></span> <span data-ttu-id="4ee72-162">Единица, уровень и/или порядковый номер, выбранный для каждого объекта, обновляется на заданное значение приращения.</span><span class="sxs-lookup"><span data-stu-id="4ee72-162">The unit, level, and/or sequence number that is selected for each entity is updated by the specified increment.</span></span>

#### <a name="sorting"></a><span data-ttu-id="4ee72-163">Сортировка</span><span class="sxs-lookup"><span data-stu-id="4ee72-163">Sorting</span></span>
<span data-ttu-id="4ee72-164">Для просмотра списка объектов в порядке последовательности можно использовать параметр **Сортировать по**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-164">Use can use the **Sort by** option to view the entity list in sequential order.</span></span>

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a><span data-ttu-id="4ee72-165">Проверка правильности сопоставления исходных данных и целевых данных</span><span class="sxs-lookup"><span data-stu-id="4ee72-165">Validate that the source data and target data are mapped correctly</span></span>
<span data-ttu-id="4ee72-166">Сопоставление — это функция, которая применяется и к заданиям импорта, и к заданиям экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-166">Mapping is a function that applies to both import and export jobs.</span></span>

- <span data-ttu-id="4ee72-167">В контексте задания импорта сопоставление описывает, какие столбцы в исходном файле становятся столбцами в промежуточной таблице.</span><span class="sxs-lookup"><span data-stu-id="4ee72-167">In the context of an import job, mapping describes which columns in the source file become the columns in the staging table.</span></span> <span data-ttu-id="4ee72-168">Таким образом система может определить, в какой столбец в промежуточной таблице должны копироваться данные того или иного столбца в исходном файле должны копироваться.</span><span class="sxs-lookup"><span data-stu-id="4ee72-168">Therefore, the system can determine which column data in the source file must be copied into which column of the staging table.</span></span>
- <span data-ttu-id="4ee72-169">В контексте задания экспорта сопоставление описывает, какие столбцы промежуточной таблицы (т. е. источника) становятся столбцами в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="4ee72-169">In the context of an export job, mapping describes which columns of the staging table (that is, the source) become the columns in the target file.</span></span>

<span data-ttu-id="4ee72-170">Если имена столбцов в промежуточной таблице и файле совпадают, система устанавливает сопоставления автоматически на основании имен.</span><span class="sxs-lookup"><span data-stu-id="4ee72-170">If the column names in the staging table and the file match, the system automatically establishes the mapping, based on the names.</span></span> <span data-ttu-id="4ee72-171">Однако, если имена различаются, столбцы не сопоставляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="4ee72-171">However, if the names differ, columns aren’t mapped automatically.</span></span> <span data-ttu-id="4ee72-172">В этих случаях необходимо выполнить сопоставление, выбрав команду **Просмотр карты** в объекте в задании данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-172">In these cases, you must complete the mapping by selecting the **View map** option on the entity in the data job.</span></span>

<span data-ttu-id="4ee72-173">Доступно два представления сопоставления: **Визуализация сопоставления**, которое используется по умолчанию, и **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-173">There are two mapping views: **Mapping visualization**, which is the default view, and **Mapping details**.</span></span> <span data-ttu-id="4ee72-174">Красной звездочкой (\*) обозначаются все обязательные поля в объекте.</span><span class="sxs-lookup"><span data-stu-id="4ee72-174">A red asterisk (\*) identifies any required fields in the entity.</span></span> <span data-ttu-id="4ee72-175">Эти поля должны быть сопоставлены, прежде чем вы сможете работать с объектом.</span><span class="sxs-lookup"><span data-stu-id="4ee72-175">These fields must be mapped before you can work with the entity.</span></span> <span data-ttu-id="4ee72-176">Работая с объектом, вы можете отменить сопоставление других полей, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="4ee72-176">You can unmap other fields as you require when you work with the entity.</span></span> <span data-ttu-id="4ee72-177">Чтобы отменить сопоставление поля, выберите поле в столбце **Объект** или в столбце **Источник**, а затем выберите **Удалить выбор**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-177">To unmap a field, select the field in either the **Entity** column or the **Source** column, and then select **Delete selection**.</span></span> <span data-ttu-id="4ee72-178">Выберите **Сохранить**, чтобы сохранить изменения, а затем закройте страницу, чтобы вернуться в проект.</span><span class="sxs-lookup"><span data-stu-id="4ee72-178">Select **Save** to save your changes, and then close the page to return to the project.</span></span> <span data-ttu-id="4ee72-179">Эту же процедуру можно использовать для изменения сопоставления полей между источником и промежуточной таблицей после импорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-179">You can use the same process to edit the field mapping from source to staging after you import.</span></span>

<span data-ttu-id="4ee72-180">Сопоставление на странице можно сгенерировать, выбрав **Создать сопоставление источника**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-180">You can generate a mapping on the page by selecting **Generate source mapping**.</span></span> <span data-ttu-id="4ee72-181">Сгенерированное сопоставление ведет себя как автоматическое сопоставление.</span><span class="sxs-lookup"><span data-stu-id="4ee72-181">A generated mapping behaves like an automatic mapping.</span></span> <span data-ttu-id="4ee72-182">Следовательно, все несопоставленные поля необходимо сопоставить вручную.</span><span class="sxs-lookup"><span data-stu-id="4ee72-182">Therefore, you must manually map any unmapped fields.</span></span>

![Сопоставление данных](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a><span data-ttu-id="4ee72-184">Проверка параметров безопасности для задания импорта или экспорта</span><span class="sxs-lookup"><span data-stu-id="4ee72-184">Verify the security for your import or export job</span></span>
<span data-ttu-id="4ee72-185">Доступ к рабочей области **Управление данными** можно ограничить, чтобы пользователи, не являющиеся администраторами, имели доступ только к определенным заданиям данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-185">Access to the **Data management** workspace can be restricted, so that non-administrator users can access only specific data jobs.</span></span> <span data-ttu-id="4ee72-186">Доступ к заданию данных подразумевает полный доступ к истории выполнения этого задания и доступ к промежуточной таблице.</span><span class="sxs-lookup"><span data-stu-id="4ee72-186">Access to a data job implies full access to the execution history of that job and access to the staging tables.</span></span> <span data-ttu-id="4ee72-187">Следовательно, при создании задания данных необходимо проследить за тем, чтобы были заданы надлежащие параметры управления доступом.</span><span class="sxs-lookup"><span data-stu-id="4ee72-187">Therefore, you must make sure that appropriate access controls are in place when you create a data job.</span></span>

### <a name="secure-a-job-by-roles-and-users"></a><span data-ttu-id="4ee72-188">Ограничение доступа к заданию по ролям и пользователям</span><span class="sxs-lookup"><span data-stu-id="4ee72-188">Secure a job by roles and users</span></span>
<span data-ttu-id="4ee72-189">Меню **Применимые роли** служит для ограничения доступа к заданию одной или несколькими ролями безопасности.</span><span class="sxs-lookup"><span data-stu-id="4ee72-189">Use the **Applicable roles** menu to restrict the job to one or more security roles.</span></span> <span data-ttu-id="4ee72-190">Доступ к заданию будут иметь только пользователи с этими ролями.</span><span class="sxs-lookup"><span data-stu-id="4ee72-190">Only users in those roles will have access to the job.</span></span>

<span data-ttu-id="4ee72-191">Также можно ограничить доступ к заданию конкретным набором пользователей.</span><span class="sxs-lookup"><span data-stu-id="4ee72-191">You can also restrict a job to specific users.</span></span> <span data-ttu-id="4ee72-192">Предоставление доступа к заданию по отдельным пользователям, а не по ролям обеспечивает более высокий уровень контроля, если роли назначено несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="4ee72-192">When you secure a job by users instead of roles, there is more control if multiple users are assigned to a role.</span></span>

### <a name="secure-a-job-by-legal-entity"></a><span data-ttu-id="4ee72-193">Ограничение доступа к заданию по юридическому лицу</span><span class="sxs-lookup"><span data-stu-id="4ee72-193">Secure a job by legal entity</span></span>
<span data-ttu-id="4ee72-194">Задания данных по природе своей являются глобальными.</span><span class="sxs-lookup"><span data-stu-id="4ee72-194">Data jobs are global in nature.</span></span> <span data-ttu-id="4ee72-195">Таким образом, при создании и использовании задания данных в юридическом лице это задание будет видно другим юридическим лицам в системе.</span><span class="sxs-lookup"><span data-stu-id="4ee72-195">Therefore, if a data job was created and used in a legal entity, the job will be visible in other legal entities in the system.</span></span> <span data-ttu-id="4ee72-196">В некоторых сценариях такое предусмотренное по умолчанию поведение является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="4ee72-196">This default behavior might be preferred in some application scenarios.</span></span> <span data-ttu-id="4ee72-197">Например, в организации, которая импортирует накладные посредством информационных объектов, может существовать централизованная группа обработки накладных, отвечающая за устранение ошибок в накладных по всем подразделениям организации.</span><span class="sxs-lookup"><span data-stu-id="4ee72-197">For example, an organization that imports invoices by using data entities might provide a centralized invoice processing team that is responsible for managing invoice errors for all divisions in the organization.</span></span> <span data-ttu-id="4ee72-198">В этом случае централизованной группе обработки накладных полезно иметь доступ к заданиям импорта накладных из всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="4ee72-198">In this scenario, it’s useful for the centralized invoice processing team to have access to invoice import jobs from all legal entities.</span></span> <span data-ttu-id="4ee72-199">Следовательно, предусмотренное по умолчанию поведение соответствует требованиям с точки зрения юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="4ee72-199">Therefore, the default behavior meets the requirement from a legal entity perspective.</span></span>

<span data-ttu-id="4ee72-200">Однако в организации также могут быть отдельные группы обработки накладных для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="4ee72-200">However, an organization might want to have invoice processing teams per legal entity.</span></span> <span data-ttu-id="4ee72-201">В таком случае команда в юридическом лице должна иметь доступ только к заданию импорта накладных в своем собственном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="4ee72-201">In this case, a team in a legal entity should have access only to the invoice import job in its own legal entity.</span></span> <span data-ttu-id="4ee72-202">Для удовлетворения этого требования можно настроить контроль доступа к заданиям данных по юридическому лицу с помощью меню **Применимые юридические лица** внутри задания данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-202">To meet this requirement, you can configure legal entity–based access control on the data jobs by using the **Applicable legal entities** menu inside the data job.</span></span> <span data-ttu-id="4ee72-203">По завершении конфигурирования пользователи смогут видеть только задания, доступные в юридическом лице, в которое они в данный момент вошли.</span><span class="sxs-lookup"><span data-stu-id="4ee72-203">After the configuration is done, users can see only jobs that are available in the legal entity that they are currently signed in to.</span></span> <span data-ttu-id="4ee72-204">Чтобы просмотреть задания в другом юридическом лице, пользователю понадобится перейти в это юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="4ee72-204">To see jobs from another legal entity, users must switch to that legal entity.</span></span>

<span data-ttu-id="4ee72-205">Доступ к заданию можно ограничить по ролям, пользователям и юридическому лицу одновременно.</span><span class="sxs-lookup"><span data-stu-id="4ee72-205">A job can be secured by roles, users, and legal entity at the same time.</span></span>

## <a name="run-the-import-or-export-job"></a><span data-ttu-id="4ee72-206">Запуск задания импорта или экспорта</span><span class="sxs-lookup"><span data-stu-id="4ee72-206">Run the import or export job</span></span>
<span data-ttu-id="4ee72-207">Можно запустить задание однократно, нажав кнопку **Импорт** или **Экспорт** после определения задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-207">You can run a job one time by selecting the **Import** or **Export** button after you define the job.</span></span> <span data-ttu-id="4ee72-208">Чтобы настроить повторяющееся задание, нажмите кнопку **Создать повторяющееся задание данных**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-208">To set up a recurring job, select **Create recurring data job**.</span></span>

## <a name="validate-that-the-job-ran-as-expected"></a><span data-ttu-id="4ee72-209">Проверка правильности выполнения задания</span><span class="sxs-lookup"><span data-stu-id="4ee72-209">Validate that the job ran as expected</span></span>
<span data-ttu-id="4ee72-210">Для исследования и устранения неполадок и в заданиях импорта, и в заданиях экспорта ведется история задания.</span><span class="sxs-lookup"><span data-stu-id="4ee72-210">The job history is available for troubleshooting and investigation on both import and export jobs.</span></span> <span data-ttu-id="4ee72-211">Запуски задания в ней упорядочены по временным диапазонам.</span><span class="sxs-lookup"><span data-stu-id="4ee72-211">Historical job runs are organized by time ranges.</span></span>

![Диапазоны в истории задания](./media/dixf-job-history.md.png)

<span data-ttu-id="4ee72-213">По каждому запуску задания фиксируются следующие подробности:</span><span class="sxs-lookup"><span data-stu-id="4ee72-213">Each job run provides the following details:</span></span>

- <span data-ttu-id="4ee72-214">Сведения о выполнении</span><span class="sxs-lookup"><span data-stu-id="4ee72-214">Execution details</span></span>
- <span data-ttu-id="4ee72-215">Журнал выполнения</span><span class="sxs-lookup"><span data-stu-id="4ee72-215">Execution log</span></span>

<span data-ttu-id="4ee72-216">Сведения о выполнении отражают состояние каждого информационного объекта, обработанного заданием.</span><span class="sxs-lookup"><span data-stu-id="4ee72-216">Execution details show the state of each data entity that the job processed.</span></span> <span data-ttu-id="4ee72-217">Таким образом можно быстро найти следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="4ee72-217">Therefore, you can quickly find the following information:</span></span>

- <span data-ttu-id="4ee72-218">Какие объекты были обработаны</span><span class="sxs-lookup"><span data-stu-id="4ee72-218">Which entities were processed</span></span>
- <span data-ttu-id="4ee72-219">Сколько записей в каждом объекте было успешно обработано, а сколько обработать не удалось</span><span class="sxs-lookup"><span data-stu-id="4ee72-219">For an entity, how many records were successfully processed, and how many failed</span></span>
- <span data-ttu-id="4ee72-220">Записи промежуточной таблицы для каждого объекта</span><span class="sxs-lookup"><span data-stu-id="4ee72-220">The staging records for each entity</span></span>

<span data-ttu-id="4ee72-221">Промежуточные данные можно загрузить в виде файла для заданий экспорта и в виде пакета для задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-221">You can download the staging data in a file for export jobs, or you can download it as a package for import and export jobs.</span></span>

<span data-ttu-id="4ee72-222">Из сведений о выполнении можно также открыть журнал выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ee72-222">From the execution details, you can also open the execution log.</span></span>

## <a name="clean-up-the-staging-tables"></a><span data-ttu-id="4ee72-223">Очистка промежуточных таблиц</span><span class="sxs-lookup"><span data-stu-id="4ee72-223">Clean up the staging tables</span></span>
<span data-ttu-id="4ee72-224">Очистить промежуточные таблицы можно с помощью функции **Очистка промежуточных данных** в рабочей области **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="4ee72-224">You can clean up staging tables by using the **Staging clean up** feature in the **Data management** workspace.</span></span> <span data-ttu-id="4ee72-225">Для выбора того, какие записи должны быть удалены из тех или иных промежуточных таблиц, можно использовать следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="4ee72-225">You can use the following options to select which records should be deleted from which staging table:</span></span>

- <span data-ttu-id="4ee72-226">**Объект** — если указан только объект, удаляются все записи из промежуточной таблицы этого объекта.</span><span class="sxs-lookup"><span data-stu-id="4ee72-226">**Entity** – If only an entity is provided, all records from that entity’s staging table are deleted.</span></span> <span data-ttu-id="4ee72-227">Выбирайте этот вариант, чтобы удалить все данные для объекта по всем проектам данных и всем заданиям.</span><span class="sxs-lookup"><span data-stu-id="4ee72-227">Select this option to clean up all the data for the entity across all data projects and all jobs.</span></span>
- <span data-ttu-id="4ee72-228">**Код задания** — если указан только код задания, все записи для всех объектов в выбранном задании удаляются из соответствующих промежуточных таблиц.</span><span class="sxs-lookup"><span data-stu-id="4ee72-228">**Job ID** – If only a job ID is provided, all records for all entities in the selected job are deleted from the appropriate staging tables.</span></span>
- <span data-ttu-id="4ee72-229">**Проекты данных** — если только выбран проект данных, удаляются все записи для всех объектов и во всех заданиях для выбранного проекта данных.</span><span class="sxs-lookup"><span data-stu-id="4ee72-229">**Data projects** – If only a data project is selected, all records for all entities and across all jobs for the selected data project are deleted.</span></span>

<span data-ttu-id="4ee72-230">Можно также сочетать эти варианты для дальнейшего ограничения удаляемого набора записей.</span><span class="sxs-lookup"><span data-stu-id="4ee72-230">You can also combine the options to further restrict the record set that is deleted.</span></span>
