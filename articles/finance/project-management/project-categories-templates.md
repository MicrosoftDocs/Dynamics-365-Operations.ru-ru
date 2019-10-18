---
title: Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation
description: В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 Finance и Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250515"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="bdd46-103">Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bdd46-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bdd46-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Dynamics 365 Finance и Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="bdd46-105">В версии 8.0 доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.</span><span class="sxs-lookup"><span data-stu-id="bdd46-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="bdd46-106">Интеграция фактических данных доступна в версии 8.0.1 или новее.</span><span class="sxs-lookup"><span data-stu-id="bdd46-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="bdd46-107">При использовании Enterprise edition 7.3.0 после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки.</span><span class="sxs-lookup"><span data-stu-id="bdd46-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="bdd46-108">Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить КБ 4131710.</span><span class="sxs-lookup"><span data-stu-id="bdd46-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="bdd46-109">Поток данных для Project Service Automation для Finance</span><span class="sxs-lookup"><span data-stu-id="bdd46-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="bdd46-110">Решение по интеграции Project Service Automation и Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="bdd46-111">Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по категориям проводок затрат проекта между Finance и Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="bdd46-112">Если категории расходов по проекту освоены в Finance, поток интеграции сначала начинается из Finance идет в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="bdd46-113">Идентификаторы интеграции категорий затрат по проекту затем обновляются путем синхронизации из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bdd46-114">Если категории расходов по проекту освоены в Project Service Automation, поток интеграции сначала начинается из Project Service Automation и идет в Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="bdd46-115">Категории проекта должны быть уже сконфигурированы в Finance до синхронизации из Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="bdd46-116">Затем выполните синхронизацию из Finance обратно в Project Service Automation, а затем из Automation Service Service снова в Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="bdd46-117">Таким образом вы помогаете гарантировать, что категории связаны, и что повторения не создаются.</span><span class="sxs-lookup"><span data-stu-id="bdd46-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="bdd46-118">Как правило, категории расходов по проекту осваиваются в Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="bdd46-119">Тем не менее, если не они не освоены или если категории расходов уже были созданы в Project Service Automation, необходимо сначала синхронизировать с помощью шаблона категорий проводок расходов по проекту (PSA в Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="bdd46-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="bdd46-120">Затем синхронизируйте с помощью шаблона категорий транзакций расходов по проекту (Fin and Ops и PSA)</span><span class="sxs-lookup"><span data-stu-id="bdd46-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="bdd46-121">Затем следует выполнить синхронизацию из Project Service Automation в Finance еще раз.</span><span class="sxs-lookup"><span data-stu-id="bdd46-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="bdd46-122">Если синхронизировать сначала из Project Service Automation, следующие требования должны быть выполнены в Finance перед выполнением синхронизации:</span><span class="sxs-lookup"><span data-stu-id="bdd46-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="bdd46-123">Должны существовать общие категории, совпадающие с категорией проекта, настроенной в Project Service Automation, и она должна быть включена как для **Проект**, так и для **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="bdd46-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="bdd46-124">Для каждого юридического лица Finance, с которым необходима интеграция, должны существовать следующие категории проекта:</span><span class="sxs-lookup"><span data-stu-id="bdd46-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="bdd46-125">**Категория проекта** существует.</span><span class="sxs-lookup"><span data-stu-id="bdd46-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="bdd46-126">**Использовать в расходах** включен.</span><span class="sxs-lookup"><span data-stu-id="bdd46-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="bdd46-127">**Активно в журнале** включен.</span><span class="sxs-lookup"><span data-stu-id="bdd46-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="bdd46-128">**Тип проводки** имеет значение **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="bdd46-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="bdd46-129">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="bdd46-130">[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="bdd46-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="bdd46-131">Синхронизация категорий расходов проекта из Finance в Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bdd46-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bdd46-132">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="bdd46-132">Template and task</span></span>

<span data-ttu-id="bdd46-133">Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="bdd46-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="bdd46-134">Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Finance в Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="bdd46-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="bdd46-135">**Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (Fin and Ops и PSA)</span><span class="sxs-lookup"><span data-stu-id="bdd46-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="bdd46-136">**Название задачи в проекте:** Синхронизация категорий в PSA</span><span class="sxs-lookup"><span data-stu-id="bdd46-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="bdd46-137">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="bdd46-137">Entity set</span></span>

| <span data-ttu-id="bdd46-138">Финансы</span><span class="sxs-lookup"><span data-stu-id="bdd46-138">Finance</span></span>                           | <span data-ttu-id="bdd46-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bdd46-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="bdd46-140">Объект интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="bdd46-140">Integration entity for categories</span></span> | <span data-ttu-id="bdd46-141">Категории проводок</span><span class="sxs-lookup"><span data-stu-id="bdd46-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="bdd46-142">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="bdd46-142">Entity flow</span></span>

<span data-ttu-id="bdd46-143">Категории расходов проекта управляются в Finance синхронизируются с Project Service Automation как категории проводок.</span><span class="sxs-lookup"><span data-stu-id="bdd46-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="bdd46-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="bdd46-144">Power Query</span></span>

<span data-ttu-id="bdd46-145">При синхронизации в Project Service Automation необходимо использовать Microsoft Power Query для Excel, чтобы настроить тип выставления счетов для категории транзакции.</span><span class="sxs-lookup"><span data-stu-id="bdd46-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="bdd46-146">В шаблоне проводок расходов проекта (Fin and Ops в PSA) предусмотрены столбец по умолчанию и сопоставление.</span><span class="sxs-lookup"><span data-stu-id="bdd46-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="bdd46-147">При создании собственного шаблона, необходимо добавить столбец с условиями в Power Query.</span><span class="sxs-lookup"><span data-stu-id="bdd46-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="bdd46-148">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bdd46-148">Follow these steps.</span></span>

1. <span data-ttu-id="bdd46-149">Щелкните стрелку, чтобы открыть сопоставление задачи категорий расходов по проекту в шаблон категорий проводок расходов по проекту (Fin and Ops в PSA).</span><span class="sxs-lookup"><span data-stu-id="bdd46-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="bdd46-150">Щелкните ссылку **Расширенный запрос и фильтрация**, чтобы открыть Power Query.</span><span class="sxs-lookup"><span data-stu-id="bdd46-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="bdd46-151">Выберите **Добавить столбец с условиями**.</span><span class="sxs-lookup"><span data-stu-id="bdd46-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="bdd46-152">Введите имя для нового столбца, например **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="bdd46-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="bdd46-153">Ввести следующее условие: **если CATEGORYID не равно null, то 19235001, иначе null**.</span><span class="sxs-lookup"><span data-stu-id="bdd46-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="bdd46-154">Щелкните **OK** в столбце.</span><span class="sxs-lookup"><span data-stu-id="bdd46-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="bdd46-155">Убедитесь, что вы провели соответствие этого нового столбца на странице соответствия.</span><span class="sxs-lookup"><span data-stu-id="bdd46-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="bdd46-156">На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="bdd46-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="bdd46-157">Соответствие показывает, какие данные полей будут синхронизированы из Finance в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="bdd46-158">[![Соответствие шаблона](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bdd46-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="bdd46-159">Синхронизация категорий расходов проекта из Project Service Automation в Finance</span><span class="sxs-lookup"><span data-stu-id="bdd46-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bdd46-160">Шаблон и задача</span><span class="sxs-lookup"><span data-stu-id="bdd46-160">Template and task</span></span>

<span data-ttu-id="bdd46-161">Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Project Service Automation в Finance:</span><span class="sxs-lookup"><span data-stu-id="bdd46-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="bdd46-162">**Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (PSA в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bdd46-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="bdd46-163">**Название задачи в проекте:** Синхронизация категорий в Fin Ops</span><span class="sxs-lookup"><span data-stu-id="bdd46-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="bdd46-164">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="bdd46-164">Entity set</span></span>

| <span data-ttu-id="bdd46-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bdd46-165">Project Service Automation</span></span> | <span data-ttu-id="bdd46-166">Финансы</span><span class="sxs-lookup"><span data-stu-id="bdd46-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="bdd46-167">Категории проводок</span><span class="sxs-lookup"><span data-stu-id="bdd46-167">Transaction categories</span></span>     | <span data-ttu-id="bdd46-168">Объект интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="bdd46-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="bdd46-169">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="bdd46-169">Entity flow</span></span>

<span data-ttu-id="bdd46-170">Категории расходов проекта управляются в Finance синхронизируются с Project Service Automation как категории проводок.</span><span class="sxs-lookup"><span data-stu-id="bdd46-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="bdd46-171">Обратная синхронизация в Finance обновляет категорию проекта в Finance с использованием кода интеграции из Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bdd46-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bdd46-172">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="bdd46-172">Template mapping in Data integration</span></span>

<span data-ttu-id="bdd46-173">На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="bdd46-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="bdd46-174">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.</span><span class="sxs-lookup"><span data-stu-id="bdd46-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bdd46-175">[![Соответствие шаблона](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bdd46-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
