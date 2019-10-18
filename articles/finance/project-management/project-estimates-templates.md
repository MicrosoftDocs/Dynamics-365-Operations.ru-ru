---
title: Синхронизация оценок по проекту напрямую из Project Service Automation в Finance and Operations
description: В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации оценок часов и оценок расходов по проекту непосредственно из Microsoft Dynamics 365 Project Service Automation в Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250492"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="79aa5-103">Синхронизация оценок по проекту напрямую из Project Service Automation в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="79aa5-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="79aa5-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации оценок часов и оценок расходов по проекту непосредственно из Dynamics 365 Project Service Automation в Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="79aa5-105">В версии 8.0 доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.</span><span class="sxs-lookup"><span data-stu-id="79aa5-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="79aa5-106">Интеграция фактических данных доступна в версии 8.0.1 или новее.</span><span class="sxs-lookup"><span data-stu-id="79aa5-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="79aa5-107">Поток данных для Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="79aa5-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="79aa5-108">Решение по интеграции Project Service Automation с Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="79aa5-109">Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по оценкам часов и оценкам расходов по проекту из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="79aa5-110">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="79aa5-111">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="79aa5-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="79aa5-112">Оценки часов по проекту</span><span class="sxs-lookup"><span data-stu-id="79aa5-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="79aa5-113">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="79aa5-113">Template and tasks</span></span>

<span data-ttu-id="79aa5-114">Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="79aa5-115">Следующий шаблон и базовые задачи используются для синхронизации оценок часов из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="79aa5-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="79aa5-116">**Имя шаблона в интеграции данных:** Оценки часов по проекту (PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="79aa5-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="79aa5-117">**Имя задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="79aa5-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="79aa5-118">Связи транзакции</span><span class="sxs-lookup"><span data-stu-id="79aa5-118">Transaction relationships</span></span>
    - <span data-ttu-id="79aa5-119">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="79aa5-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="79aa5-120">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="79aa5-120">Entity set</span></span>

| <span data-ttu-id="79aa5-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="79aa5-121">Project Service Automation</span></span> | <span data-ttu-id="79aa5-122">Финансы</span><span class="sxs-lookup"><span data-stu-id="79aa5-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="79aa5-123">Задачи по проекту</span><span class="sxs-lookup"><span data-stu-id="79aa5-123">Project tasks</span></span>              | <span data-ttu-id="79aa5-124">Объект интеграции для оценки часов проекта</span><span class="sxs-lookup"><span data-stu-id="79aa5-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="79aa5-125">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="79aa5-125">Entity flow</span></span>

<span data-ttu-id="79aa5-126">Оценки часов проекта управляются в Project Service Automation и синхронизируются с Finance как прогнозы часов проекта.</span><span class="sxs-lookup"><span data-stu-id="79aa5-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="79aa5-127">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="79aa5-127">Prerequisites</span></span>

<span data-ttu-id="79aa5-128">Прежде чем синхронизация оценок часа проекта может произойти, вы должны синхронизировать проекты, проектные задачи и категории проводок затрат по проекту.</span><span class="sxs-lookup"><span data-stu-id="79aa5-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="79aa5-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="79aa5-129">Power Query</span></span>

<span data-ttu-id="79aa5-130">В шаблоне оценок часов проекта необходимо использовать Microsoft Power Query для Excel для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="79aa5-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="79aa5-131">Установите код модели прогноза по умолчанию, который будет использоваться, когда интеграции будет создавать новые прогнозы часов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="79aa5-132">Отфильтруйте любые записи, относящиеся к определенному ресурсу, в рамках задачи, которая не сможет осуществить интеграцию в прогнозы часов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="79aa5-133">Отфильтруйте все строки категории пустой транзакции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="79aa5-134">Невыполнение этой задачи может привести к неправильным прогнозам часов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="79aa5-135">Задание кода прогнозной модели по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79aa5-135">Set the default forecast model ID</span></span>

<span data-ttu-id="79aa5-136">Чтобы обновить вставленный в шаблон код прогнозной модели по умолчанию, щелкните стрелку **Сопоставить**, чтобы открыть соответствие.</span><span class="sxs-lookup"><span data-stu-id="79aa5-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="79aa5-137">Затем выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="79aa5-138">При использовании шаблона по умолчанию для шаблона оценок часов проекта (PSA и Fin and Ops) выберите **Вставленное условие** в списке **Примененные действия**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="79aa5-139">В записи **Функция** замените **O\_forecast** на имя код прогнозной модели, которое должно использоваться при интеграции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="79aa5-140">Шаблон по умолчанию содержит код прогнозной модели в демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="79aa5-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="79aa5-141">При создании нового шаблона необходимо добавить этот столбец.</span><span class="sxs-lookup"><span data-stu-id="79aa5-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="79aa5-142">В Power Query выберите **Добавить столбец с условиями** и введите имя для нового столбца, такое как **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="79aa5-143">Введите условие для столбца, где, если задача проекта не равна null, затем \<введите код прогнозной модели\>; в противном случае null.</span><span class="sxs-lookup"><span data-stu-id="79aa5-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="79aa5-144">Отфильтровать определенные записи ресурсов</span><span class="sxs-lookup"><span data-stu-id="79aa5-144">Filter out resource-specific records</span></span>

<span data-ttu-id="79aa5-145">Шаблон (PSA и Fin and Ops) оценок часов по проекту имеет фильтр по умолчанию, который удаляет любую конкретную запись ресурса предположительно создаваемого проекта.</span><span class="sxs-lookup"><span data-stu-id="79aa5-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="79aa5-146">При создании собственного шаблона, необходимо добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="79aa5-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="79aa5-147">Выберите ссылку **Расширенный запрос и фильтрация** для фильтрации по столбцу **msdyn\_islinetask**, чтобы только записи **False** (Ложь) были включены.</span><span class="sxs-lookup"><span data-stu-id="79aa5-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="79aa5-148">Отфильтруйте все строки категории пустой транзакции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="79aa5-149">Необходимо добавить фильтр, чтобы удалить все строки, которые содержат категории пустых проводок.</span><span class="sxs-lookup"><span data-stu-id="79aa5-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="79aa5-150">Эта задача обязательна, независимо от того, используете ли вы шаблон по умолчанию или создали свой собственный шаблон.</span><span class="sxs-lookup"><span data-stu-id="79aa5-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="79aa5-151">Этот фильтр удаляет любые сводные строки, поступающие из Project Service Automation, которые могут привести к неверным прогнозам часов в Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="79aa5-152">Выберите ссылку **Расширенный запрос и фильтрация**, чтобы отфильтровать записи со значением null в столбце **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="79aa5-153">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="79aa5-153">Template mapping in Data integration</span></span>

<span data-ttu-id="79aa5-154">На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="79aa5-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="79aa5-155">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="79aa5-156">[![Соответствие шаблона](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="79aa5-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="79aa5-157">Оценки расходов по проектам</span><span class="sxs-lookup"><span data-stu-id="79aa5-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="79aa5-158">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="79aa5-158">Template and tasks</span></span>

<span data-ttu-id="79aa5-159">Следующий шаблон и базовые задачи используются для синхронизации оценок расходов по проекту из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="79aa5-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="79aa5-160">**Имя шаблона в интеграции данных:** Оценки расходов по проекту (PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="79aa5-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="79aa5-161">**Имя задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="79aa5-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="79aa5-162">Связи транзакции</span><span class="sxs-lookup"><span data-stu-id="79aa5-162">Transaction relationships</span></span> 
    - <span data-ttu-id="79aa5-163">Оценки расходов</span><span class="sxs-lookup"><span data-stu-id="79aa5-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="79aa5-164">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="79aa5-164">Entity set</span></span>

| <span data-ttu-id="79aa5-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="79aa5-165">Project Service Automation</span></span> | <span data-ttu-id="79aa5-166">Финансы</span><span class="sxs-lookup"><span data-stu-id="79aa5-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="79aa5-167">Связи проводок</span><span class="sxs-lookup"><span data-stu-id="79aa5-167">Transaction Connections</span></span>    | <span data-ttu-id="79aa5-168">Объект интеграции для связей проводок по проекту</span><span class="sxs-lookup"><span data-stu-id="79aa5-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="79aa5-169">Строки оценки</span><span class="sxs-lookup"><span data-stu-id="79aa5-169">Estimate Lines</span></span>             | <span data-ttu-id="79aa5-170">Объект интеграции для оценок расходов проекта</span><span class="sxs-lookup"><span data-stu-id="79aa5-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="79aa5-171">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="79aa5-171">Entity flow</span></span>

<span data-ttu-id="79aa5-172">Оценки расходов проекта управляются в Project Service Automation и синхронизируются с Finance как прогнозы расходов проекта.</span><span class="sxs-lookup"><span data-stu-id="79aa5-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="79aa5-173">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="79aa5-173">Prerequisites</span></span>

<span data-ttu-id="79aa5-174">Прежде чем синхронизация оценок расходов проекта может произойти, вы должны синхронизировать проекты, проектные задачи и категории проводок затрат по проекту.</span><span class="sxs-lookup"><span data-stu-id="79aa5-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="79aa5-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="79aa5-175">Power Query</span></span>

<span data-ttu-id="79aa5-176">В шаблоне оценок расходов по проекту необходимо использовать Power Query для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="79aa5-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="79aa5-177">Отфильтруйте для включения только записей оценки расходов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="79aa5-178">Установите код модели прогноза по умолчанию, который будет использоваться, когда интеграции будет создавать новые прогнозы часов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="79aa5-179">Преобразование типов выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="79aa5-179">Transform the billing types.</span></span>
- <span data-ttu-id="79aa5-180">Преобразование типов проводок.</span><span class="sxs-lookup"><span data-stu-id="79aa5-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="79aa5-181">Отфильтруйте для включения только строк оценки расходов</span><span class="sxs-lookup"><span data-stu-id="79aa5-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="79aa5-182">Шаблон (СРП Fin и Ops) оценки расходов проекта имеет фильтр по умолчанию, который включает только строки расходов в интеграцию.</span><span class="sxs-lookup"><span data-stu-id="79aa5-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="79aa5-183">При создании собственного шаблона, необходимо добавить этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="79aa5-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="79aa5-184">Выберите задачу **Связи транзакции**, затем щелкните стрелку **Сопоставление**, чтобы открыть сопоставление.</span><span class="sxs-lookup"><span data-stu-id="79aa5-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="79aa5-185">Выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="79aa5-186">Отфильтруйте столбец **msdyn\_transactiontype1**, чтобы он включал только **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="79aa5-187">Задание кода прогнозной модели по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79aa5-187">Set the default forecast model ID</span></span>

<span data-ttu-id="79aa5-188">Чтобы обновить вставленный в шаблон код прогнозной модели по умолчанию, выберите задачу **Оценки расходов**, затем щелкните стрелку **Сопоставить**, чтобы открыть сопоставление.</span><span class="sxs-lookup"><span data-stu-id="79aa5-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="79aa5-189">Выберите ссылку **Расширенный запрос и фильтрация**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="79aa5-190">При использовании шаблона по умолчанию для оценок расходов по проекту (PSA и Fin and Ops) в Power Query выберите сначала **Вставленное условие** в разделе **Примененные действия**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="79aa5-191">В записи **Функция** замените **O\_forecast** на имя код прогнозной модели, которое должно использоваться при интеграции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="79aa5-192">Шаблон по умолчанию содержит код прогнозной модели в демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="79aa5-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="79aa5-193">При создании нового шаблона необходимо добавить этот столбец.</span><span class="sxs-lookup"><span data-stu-id="79aa5-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="79aa5-194">В Power Query выберите **Добавить столбец с условиями** и введите имя для нового столбца, такое как **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="79aa5-195">Введите условие для столбца, где код строки оценки не равен null, а затем \<введите код прогнозной модели\>; в противном случае null.</span><span class="sxs-lookup"><span data-stu-id="79aa5-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="79aa5-196">Преобразование типов выставления счетов</span><span class="sxs-lookup"><span data-stu-id="79aa5-196">Transform the billing types</span></span>

<span data-ttu-id="79aa5-197">Шаблон оценки расходов проекта (PSA и Fin and Opss) включает столбец с условиями, который используется для преобразования типов выставления счетов, полученных от Project Service Automation во время интеграции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="79aa5-198">При создании собственного шаблона, необходимо добавить этот столбец с условиями.</span><span class="sxs-lookup"><span data-stu-id="79aa5-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="79aa5-199">Выберите ссылку **Расширенный запрос и фильтрация**, затем выберите **Добавить столбец с условиями**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="79aa5-200">Введите имя для нового столбца, например **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="79aa5-201">Затем введите следующее условие:</span><span class="sxs-lookup"><span data-stu-id="79aa5-201">Then enter the following condition:</span></span>

<span data-ttu-id="79aa5-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="79aa5-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="79aa5-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="79aa5-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="79aa5-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="79aa5-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="79aa5-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="79aa5-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="79aa5-206">Преобразование типов проводок</span><span class="sxs-lookup"><span data-stu-id="79aa5-206">Transform the transaction types</span></span>

<span data-ttu-id="79aa5-207">Шаблон оценки расходов проекта (PSA и Fin and Opss) включает столбец с условиями, который используется для преобразования типов проводки, полученных от Project Service Automation во время интеграции.</span><span class="sxs-lookup"><span data-stu-id="79aa5-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="79aa5-208">При создании собственного шаблона, необходимо добавить этот столбец с условиями.</span><span class="sxs-lookup"><span data-stu-id="79aa5-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="79aa5-209">Выберите ссылку **Расширенный запрос и фильтрация**, затем выберите **Добавить столбец с условиями**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="79aa5-210">Введите имя для нового столбца, например **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="79aa5-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="79aa5-211">Затем введите следующее условие:</span><span class="sxs-lookup"><span data-stu-id="79aa5-211">Then enter the following condition:</span></span>

<span data-ttu-id="79aa5-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="79aa5-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="79aa5-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="79aa5-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="79aa5-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="79aa5-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="79aa5-215">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="79aa5-215">Template mapping in Data integration</span></span>

<span data-ttu-id="79aa5-216">На следующих рисунках показаны примеры соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="79aa5-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="79aa5-217">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="79aa5-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="79aa5-218">[![Соответствие шаблона](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="79aa5-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="79aa5-219">[![Соответствие шаблона](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="79aa5-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
