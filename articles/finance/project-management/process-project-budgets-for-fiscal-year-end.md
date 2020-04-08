---
title: Перенос бюджетов проектов в конце финансового года
description: В этой статье представлена информация о том, как перенести оставшиеся бюджетные суммы в будущие годы и создать сведения о регистре бюджета.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172338"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="fbbbe-103">Перенос бюджетов проектов в конце финансового года</span><span class="sxs-lookup"><span data-stu-id="fbbbe-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbbbe-104">При работе с многолетним проектом в конце финансового года может остаться бюджет.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="fbbbe-105">Вы можете переместить оставшиеся бюджетные суммы на будущий год и создать сведения о регистре бюджета для этих сумм на связанных счетах главной книги.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="fbbbe-106">Перед переносом оставшихся сумм проверьте и проанализируйте оставшиеся бюджетные суммы.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="fbbbe-107">Просмотр и анализ оставшихся бюджетных сумм</span><span class="sxs-lookup"><span data-stu-id="fbbbe-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="fbbbe-108">Выполните следующие действия, чтобы проверить бюджетные суммы на конце года для проектов, но пока не переносить эти суммы.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="fbbbe-109">Выберите **Управление и учет по проектам** > **Периодические** > **Бюджеты** > **Перенос бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="fbbbe-110">На странице **Процесс переноса бюджета проекта** на вкладке **Параметры конца года** убедитесь, что пункт **Перенести суммы остатков бюджета по проекту** не активирован.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="fbbbe-111">На вкладке **Параметры** в поле **Год бюджета проекта** выберите финансовый год, для которого требуется просмотреть оставшуюся бюджетную сумму.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="fbbbe-112">В поле **Начало финансового года** выберите начало финансового года, для которого требуется просмотреть оставшуюся бюджетную сумму.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="fbbbe-113">В поле **Из прогнозной модели** выберите **Оставшийся бюджет**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="fbbbe-114">Чтобы включить проекты, которые удовлетворяют выбранным критериям и не имеют остатков бюджета, установите флажок **Показать нулевые остатки**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="fbbbe-115">На вкладке **Выберите бюджеты** выберите **Извлечь все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям, затем выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="fbbbe-116">Чтобы разработать запрос к базе данных, который будет загружать в эту область определенный набор бюджетов, выберите **Извлечь выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="fbbbe-117">Для получения дополнительных сведений о конкретной строке в области выберите эту строку, затем выберите **Просмотр сведений о бюджете** или **Просмотр счетов**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="fbbbe-118">Перенести суммы остатков бюджета</span><span class="sxs-lookup"><span data-stu-id="fbbbe-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="fbbbe-119">После обработки оставшихся бюджетных сумм можно создать проводки в главной книге для сумм, переносимых на следующий год.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="fbbbe-120">Чтобы создать проводки главной книги, выполните шаги из раздела [Перенос сумм бюджета и создание проводок главной книги](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="fbbbe-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="fbbbe-121">Бюджетные суммы, переносимые на следующий год, перемещаются в прогнозную модель, которая выбрана на странице **Прогнозные модели** в качестве прогнозной модели для переноса.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="fbbbe-122">Перенос бюджетных сумм на следующий год с созданием проводок ГК</span><span class="sxs-lookup"><span data-stu-id="fbbbe-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="fbbbe-123">Выберите **Управление и учет по проектам** > **Периодические** > **Бюджеты** > **Перенос бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="fbbbe-124">На странице **Процесс переноса бюджета проекта** выберите **Конец года**, затем включите параметры **Перенести суммы остатков бюджета по проекту** и **Создать записи регистра бюджета в главной книге**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="fbbbe-125">На вкладке **Параметры** в группе полей **Параметры проекта** выберите следующее:</span><span class="sxs-lookup"><span data-stu-id="fbbbe-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="fbbbe-126">**Год бюджета проекта**: выберите начало финансового года, для которого требуется просмотреть оставшиеся бюджетные суммы.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="fbbbe-127">**Прибыли и убытки** создайте проводки прибылей и убытков в главной книге.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="fbbbe-128">**НЗП**: создайте проводки незавершенного производства (НЗП) в главной книге.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="fbbbe-129">**Зарплата**: создайте проводки распределения зарплаты в главной книге.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="fbbbe-130">В группе полей **Главная книга** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fbbbe-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="fbbbe-131">В поле **Начало финансового года** выберите финансовый год, в который требуется переместить оставшиеся бюджетные суммы для проектов.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="fbbbe-132">Значение по умолчанию — на год позже значения в поле **Год бюджета проекта**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="fbbbe-133">В поле **Период переноса** выберите период, для которого требуется создать сведения о регистре бюджета в главной книге.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="fbbbe-134">Обычно это первый период в открывающем финансовом году.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="fbbbe-135">В группе полей **Копировать из/в** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fbbbe-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="fbbbe-136">В поле **Из прогнозной модели** выберите прогнозную модель бюджета по проекту, связанную с оставшимися бюджетными суммами, которые требуется переместить для проектов.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="fbbbe-137">В поле **В бюджетную модель книги учета** выберите модель бюджета ГК, связанную с бюджетными суммами, которые требуется переместить в ГК.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="fbbbe-138">Чтобы использовать для создаваемых при перемещении бюджетных сумм для проектов проводок ГК валюту реализации проекта, выберите **Валюта продаж для переноса**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="fbbbe-139">Если этот параметр не выбран, в проводках используется валюта учета.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="fbbbe-140">Выберите **Показать нулевые остатки**, чтобы включить в проекты, по которым нет оставшихся бюджетных сумм, однако которые соответствуют другим критериям, выбранным в нижней панели.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="fbbbe-141">На вкладке **Выберите бюджеты** выберите **Извлечь все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="fbbbe-142">Если вы предпочитаете разработать запрос к базе данных, который будет загружать в эту область определенный набор бюджетов проектов, выберите **Извлечь выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="fbbbe-143">Для каждого проекта, который требуется обработать, выберите параметр в начале строки для проекта.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="fbbbe-144">Чтобы выбрать все или большинство проектов, установите флажок в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="fbbbe-145">Чтобы исключить обработку любого проекта, снимите флажок для этого проекта.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="fbbbe-146">Чтобы переместить оставшиеся бюджетные суммы для выбранных проектов на выбранный финансовый год и создать сведения о регистре бюджета в главной книге, выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="fbbbe-147">Перенос бюджетных сумм без создания проводок ГК</span><span class="sxs-lookup"><span data-stu-id="fbbbe-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="fbbbe-148">Выберите **Управление и учет по проектам** > **Периодические** > **Бюджеты** > **Перенос бюджетов**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="fbbbe-149">На странице **Процесс переноса бюджета проекта** в поле **Параметры конца года** выберите **Перенести суммы остатков бюджета по проекту**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="fbbbe-150">В группе **Параметры** в поле **Год бюджета проекта** выберите финансовый год, для которого требуется просмотреть оставшиеся бюджетные суммы.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="fbbbe-151">В группе **Копировать из/в** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fbbbe-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="fbbbe-152">В поле **Из прогнозной модели** выберите прогнозную модель бюджета по проекту, связанную с оставшимися бюджетными суммами, которые требуется переместить для проектов.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="fbbbe-153">Выберите **Показать нулевые остатки**, чтобы включить проекты, которые не имеют остатков бюджета, но удовлетворяют другим выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="fbbbe-154">В группе **Выберите бюджеты** выберите **Извлечь все бюджеты**, чтобы загрузить все бюджеты, соответствующие выбранным критериям.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="fbbbe-155">Чтобы разработать запрос к базе данных, который будет загружать в эту область определенный набор бюджетов проектов, выберите **Извлечь выбранные бюджеты**.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="fbbbe-156">Для каждого проекта, который требуется обработать, выберите параметр в начале строки для проекта.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="fbbbe-157">Выберите **Обработать**, чтобы переместить оставшиеся бюджетные суммы для выбранных проектов в выбранный финансовый год.</span><span class="sxs-lookup"><span data-stu-id="fbbbe-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

