---
title: "Синхронизация категорий расходов проекта из Project Service Automation"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 for Finance and Operations и Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ru-ru
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="08d03-103">Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="08d03-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="08d03-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 for Finance and Operations и Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="08d03-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="08d03-105">Dynamics 365 for Finance and Operations версии 8.0. доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.</span><span class="sxs-lookup"><span data-stu-id="08d03-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="08d03-106">Поток данных для Project Service Automation и Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08d03-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="08d03-107">Решение по интеграции Project Service Automation и Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="08d03-108">Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по категориям проводок затрат проекта Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="08d03-109">Если категории расходов по проекту освоены в Finance and Operations, поток интеграции сначала происходит из Finance and Operations в Project Service Automation, а затем обновляются идентификаторы интеграции категорий расходов проекта в результате синхронизации из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="08d03-110">Если категории расходов по проекту освоены в Project Service Automation, поток интеграции сначала начинается из Project Service Automation и идет в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="08d03-111">Категории проекта должны быть уже сконфигруированы в Finance and Operations до синхронизации из Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="08d03-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="08d03-112">Затем выполните синхронизацию из Finance and Operations обратно в Project Service Automation, а затем из Automation Service Service снова в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="08d03-113">Это гарантирует, что категории будут связаны и не создадутся дубликаты.</span><span class="sxs-lookup"><span data-stu-id="08d03-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="08d03-114">Как правило, категории расходов по проекту будут освоены в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="08d03-115">Если это не ваша ситуация или у вас уже есть категории затрат, созданные в Project Service Automation, вы должны сначала синхронизировать, используя категории проводок затрат по проекту (PSA и Fin и Ops), а затем синхронизировать с использованием категорий транзакций затрат по проекту (Fin и Ops to PSA).</span><span class="sxs-lookup"><span data-stu-id="08d03-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="08d03-116">Следует затем запустить синхронизацию от PSA к Fin and Ops еще раз.</span><span class="sxs-lookup"><span data-stu-id="08d03-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="08d03-117">Если осуществлять синхронизацию сначала из Project Service Automation, категорий проекта должны уже быть настроены в Finance and Operations и любая категория по проекту, которая должна быть синхронизирована с категориями транзакции Project Service Automation должна быть настроена как **Активно в журналах**.</span><span class="sxs-lookup"><span data-stu-id="08d03-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="08d03-118">На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="08d03-119">[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="08d03-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="08d03-120">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="08d03-120">Templates and tasks</span></span>

<span data-ttu-id="08d03-121">Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты**и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="08d03-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="08d03-122">Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Finance and Operations в Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="08d03-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="08d03-123">**Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (Fin and Ops и PSA)</span><span class="sxs-lookup"><span data-stu-id="08d03-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="08d03-124">**Название задачи в проекте:** Синхронизация категорий в PSA</span><span class="sxs-lookup"><span data-stu-id="08d03-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="08d03-125">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="08d03-125">Entity set</span></span>

| <span data-ttu-id="08d03-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08d03-126">Finance and Operations</span></span>               | <span data-ttu-id="08d03-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="08d03-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="08d03-128">Объект интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="08d03-128">Integration entity for categories</span></span>    | <span data-ttu-id="08d03-129">Категории проводок</span><span class="sxs-lookup"><span data-stu-id="08d03-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="08d03-130">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="08d03-130">Entity flow</span></span>

<span data-ttu-id="08d03-131">Категории расходов проекта управляются в Finance and Operations синхронизируются с Project Service Automation как категории проводок.</span><span class="sxs-lookup"><span data-stu-id="08d03-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="08d03-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="08d03-132">Power Query</span></span>

<span data-ttu-id="08d03-133">Необходимо использовать Microsoft Power Query, чтобы настроить тип выставления счетов для категории транзакции при синхронизации для Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="08d03-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="08d03-134">В шаблоне проводок расходов проекта (Fin and Ops и PSA) есть столбец по умолчанию и уже имеется соответствие.</span><span class="sxs-lookup"><span data-stu-id="08d03-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="08d03-135">При создании собственного шаблона, необходимо добавить столбец с условиями в Power Query.</span><span class="sxs-lookup"><span data-stu-id="08d03-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="08d03-136">Откройте форму «Расширенный запрос и фильтрация» в рамках задания по соответствию задачи по категориям расходов проекта.</span><span class="sxs-lookup"><span data-stu-id="08d03-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="08d03-137">Выберите **Добавить столбец с условиями**.</span><span class="sxs-lookup"><span data-stu-id="08d03-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="08d03-138">Назвать новый столбец, например «BillingType».</span><span class="sxs-lookup"><span data-stu-id="08d03-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="08d03-139">Ввести следующее условие: если **CATEGORYID не равен null, затем 19235001, в противном случае — значение null**.</span><span class="sxs-lookup"><span data-stu-id="08d03-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="08d03-140">Щелкните **OK** в столбце.</span><span class="sxs-lookup"><span data-stu-id="08d03-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="08d03-141">Убедитесь, что вы провели соответствие этого нового столбца на странице соответствия.</span><span class="sxs-lookup"><span data-stu-id="08d03-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="08d03-142">На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="08d03-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="08d03-143">Соответствие показывает, какие данные полей будут синхронизированы из Finance and Operations в Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="08d03-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="08d03-144">[![Соответствие шаблона](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="08d03-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="08d03-145">Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Project Service Automation в Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="08d03-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="08d03-146">-**Имя шаблона в интеграции данных:** Категории транзакции расходов по проекту (PSA и Fin and Ops) —**Название задачи в проекте:** синхронизировать с Fin Ops</span><span class="sxs-lookup"><span data-stu-id="08d03-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="08d03-147">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="08d03-147">Entity set</span></span>

| <span data-ttu-id="08d03-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="08d03-148">Project Service Automation</span></span>      | <span data-ttu-id="08d03-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="08d03-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="08d03-150">Категории проводок</span><span class="sxs-lookup"><span data-stu-id="08d03-150">Transaction categories</span></span>          | <span data-ttu-id="08d03-151">Объект интеграции для категорий</span><span class="sxs-lookup"><span data-stu-id="08d03-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="08d03-152">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="08d03-152">Entity flow</span></span>

<span data-ttu-id="08d03-153">Категории расходов проекта управляются в Finance and Operations синхронизируются с Project Service Automation как категории проводок.</span><span class="sxs-lookup"><span data-stu-id="08d03-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="08d03-154">Обратная синхронизация в Finance and Operations обновляет интеграцию кода из Project Service Automation в категории проекта Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="08d03-155">На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="08d03-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="08d03-156">Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08d03-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="08d03-157">[![Соответствие шаблона](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="08d03-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

