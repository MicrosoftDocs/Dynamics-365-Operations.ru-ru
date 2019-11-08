---
title: Обзор управления качеством
description: Эта тема описывает, как можно использовать управление качеством в Dynamics 365 Supply Chain Management, чтобы улучшить качество продукта в вашей цепи поставок.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653564"
---
# <a name="quality-management-overview"></a><span data-ttu-id="3724e-103">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="3724e-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3724e-104">Эта тема описывает, как можно использовать управление качеством в Dynamics 365 Supply Chain Management, чтобы улучшить качество продукта в вашей цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="3724e-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="3724e-105">Управление качеством может помочь вам управлять периодами оборота, когда вы работаете с несоответствующими продуктами, независимо от их источника происхождения.</span><span class="sxs-lookup"><span data-stu-id="3724e-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="3724e-106">Поскольку диагностические типы связаны с отчетностью о коррекции, Supply Chain Management может планировать задачи для исправления проблем и предотвращения их повторения.</span><span class="sxs-lookup"><span data-stu-id="3724e-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="3724e-107">В дополнение к функциональности для управляя несоответствием, управление качеством включает функциональность для отслеживания проблем по типу проблемы (даже внутренние проблемы), и для определения решений как краткосрочные или долгосрочные.</span><span class="sxs-lookup"><span data-stu-id="3724e-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="3724e-108">Статистика по ключевым индикаторам производительности обеспечивает анализ истории предыдущих проблем несоответствия и решений, которые были применены для их исправления.</span><span class="sxs-lookup"><span data-stu-id="3724e-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="3724e-109">Вы можете использовать исторические данные для просмотра эффективности предыдущих мер по обеспечению качества и определить соответствующие меры для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="3724e-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="3724e-110">При указании сопоставления контроля качества Supply Chain Management может сформировать заказы по контролю качества для различных бизнес-процессов, событий и условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="3724e-111">Сопоставление может относиться к определенной номенклатуре, группе или ко всем продуктам.</span><span class="sxs-lookup"><span data-stu-id="3724e-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="3724e-112">Примеры использования управления качеством</span><span class="sxs-lookup"><span data-stu-id="3724e-112">Examples of the use of quality management</span></span>
<span data-ttu-id="3724e-113">Управление качеством гибкое и может быть реализована различными способами для соответствия требованиям определенных уровней операций цепочки снабжения.</span><span class="sxs-lookup"><span data-stu-id="3724e-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="3724e-114">Следующие примеры иллюстрируют возможное использование этих функций.</span><span class="sxs-lookup"><span data-stu-id="3724e-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="3724e-115">Автоматический запуск процесса контроля качества, основанный на предопределенных критериях (после регистрации на складе заказа на покупку от определенного поставщика).</span><span class="sxs-lookup"><span data-stu-id="3724e-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="3724e-116">Блокировка запасов во время проверки для исключения использования неутвержденных запасов (полная блокировка количеств по заказу на покупку).</span><span class="sxs-lookup"><span data-stu-id="3724e-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="3724e-117">Использование выборочного контроля номенклатур в рамках ассоциации качества для того, чтобы определить сумму текущих физических запасов, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="3724e-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="3724e-118">Выборочный контроль может быть основан на фиксированных количествах или на процентном объеме.</span><span class="sxs-lookup"><span data-stu-id="3724e-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="3724e-119">Создайте заказы для контроля качества для частичных приемок.</span><span class="sxs-lookup"><span data-stu-id="3724e-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="3724e-120">Чтобы создать заказ для контроля качества, основанный на количестве, физически полученном с заказом, необходимо установить флажок **На обновленное количество** в форме **Выборка элементов**.</span><span class="sxs-lookup"><span data-stu-id="3724e-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="3724e-121">Создание типов испытаний, которые включают минимальные, максимальные и целевые значения испытаний, и выполнение качественного или количественного тестирования с предопределенными результатами проверки.</span><span class="sxs-lookup"><span data-stu-id="3724e-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="3724e-122">Указание допустимого уровня качества (AQL) для управления допусками измерения качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="3724e-123">Указание ресурсов, которые требуются для контрольной операции, например испытательный участок и инструменты для испытаний.</span><span class="sxs-lookup"><span data-stu-id="3724e-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="3724e-124">Работа с сопоставлениями контроля качества</span><span class="sxs-lookup"><span data-stu-id="3724e-124">Working with quality associations</span></span>
<span data-ttu-id="3724e-125">Бизнес-процесс, использующий сопоставления, может быть связан с различными исходными документами, такими как заказы на покупку, заказы на продажу и производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="3724e-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="3724e-126">Каждая запись сопоставления качества определяет также набор тестов, AQL и план выборочного контроля, применимые для создаваемых автоматически качественных заказов.</span><span class="sxs-lookup"><span data-stu-id="3724e-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="3724e-127">Необходимо определить запись сопоставления контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="3724e-128">Например, можно создать сопоставление, которое формирует заказ контроля качества для заказов на продажу, когда обновляется поступление продуктов по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="3724e-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="3724e-129">В зависимости от настройки плана исполнения возможна блокировка самого запускающего процесса, пока имеется открытый заказ для контроля качества, или блокировка следующих процессов, таких как выставление накладной по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="3724e-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="3724e-130">**Примечание.** Пока имеются открытые заказы для контроля качества, количества запасов автоматически блокируются по выдаче.</span><span class="sxs-lookup"><span data-stu-id="3724e-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="3724e-131">В зависимости от настройки **Полная блокировка** на странице **Выборка номенклатур**, количество равно количеству в заказе для контроля качества или количеству в строке исходного документа.</span><span class="sxs-lookup"><span data-stu-id="3724e-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="3724e-132">Сопоставление по контролю качестве указывает событие и условия, при которых формируется заказ на контроль качества для определенного бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="3724e-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="3724e-133">Условия могут быть заданы для определенного места или юридического лица.</span><span class="sxs-lookup"><span data-stu-id="3724e-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="3724e-134">Заказ по контролю качества, в котором используются разрушающие испытания, может формироваться, только если для данного события имеется складской запас.</span><span class="sxs-lookup"><span data-stu-id="3724e-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="3724e-135">Следующие примеры иллюстрируют определение записи сопоставления качества для отклонений в бизнес-процессах.</span><span class="sxs-lookup"><span data-stu-id="3724e-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="3724e-136">Примеры обобщаются также в следующей таблице в плане событий и условий, определенных записью сопоставления качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3724e-137">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="3724e-137">Reference type</span></span></th>
<th><span data-ttu-id="3724e-138">Тип события</span><span class="sxs-lookup"><span data-stu-id="3724e-138">Event type</span></span></th>
<th><span data-ttu-id="3724e-139">Выполнение</span><span class="sxs-lookup"><span data-stu-id="3724e-139">Execution</span></span></th>
<th><span data-ttu-id="3724e-140">Блокировка событий</span><span class="sxs-lookup"><span data-stu-id="3724e-140">Event blocking</span></span></th>
<th><span data-ttu-id="3724e-141">Ссылка на документ</span><span class="sxs-lookup"><span data-stu-id="3724e-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3724e-142">Запасы</span><span class="sxs-lookup"><span data-stu-id="3724e-142">Inventory</span></span></td>
<td><span data-ttu-id="3724e-143">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3724e-143">Not applicable</span></span></td>
<td><span data-ttu-id="3724e-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3724e-144">Not applicable</span></span></td>
<td><span data-ttu-id="3724e-145">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-145">None</span></span></td>
<td><span data-ttu-id="3724e-146">Все</span><span class="sxs-lookup"><span data-stu-id="3724e-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="3724e-147">Прод.</span><span class="sxs-lookup"><span data-stu-id="3724e-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="3724e-148">Процесс комплектации запланирован</span><span class="sxs-lookup"><span data-stu-id="3724e-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="3724e-149">До</span><span class="sxs-lookup"><span data-stu-id="3724e-149">Before</span></span></td>
<td><span data-ttu-id="3724e-150">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="3724e-151">Только определенный код, группа или все</span><span class="sxs-lookup"><span data-stu-id="3724e-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-152">Процесс комплектации</span><span class="sxs-lookup"><span data-stu-id="3724e-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-153">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="3724e-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-154">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3724e-155">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="3724e-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-156">До</span><span class="sxs-lookup"><span data-stu-id="3724e-156">Before</span></span></td>
<td><span data-ttu-id="3724e-157">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-158">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="3724e-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-159">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="3724e-160">Покупка</span><span class="sxs-lookup"><span data-stu-id="3724e-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="3724e-161">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="3724e-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="3724e-162">До</span><span class="sxs-lookup"><span data-stu-id="3724e-162">Before</span></span></td>
<td><span data-ttu-id="3724e-163">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-164">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="3724e-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-165">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-166">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3724e-167">После</span><span class="sxs-lookup"><span data-stu-id="3724e-167">After</span></span></td>
<td><span data-ttu-id="3724e-168">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-169">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-170">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3724e-171">Регистрация</span><span class="sxs-lookup"><span data-stu-id="3724e-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-172">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3724e-172">Not applicable</span></span></td>
<td><span data-ttu-id="3724e-173">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-174">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-175">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3724e-176">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-177">До</span><span class="sxs-lookup"><span data-stu-id="3724e-177">Before</span></span></td>
<td><span data-ttu-id="3724e-178">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-179">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-180">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3724e-181">После</span><span class="sxs-lookup"><span data-stu-id="3724e-181">After</span></span></td>
<td><span data-ttu-id="3724e-182">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-183">Счет</span><span class="sxs-lookup"><span data-stu-id="3724e-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="3724e-184">Производство</span><span class="sxs-lookup"><span data-stu-id="3724e-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-185">Регистрация</span><span class="sxs-lookup"><span data-stu-id="3724e-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-186">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3724e-186">Not applicable</span></span></td>
<td><span data-ttu-id="3724e-187">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="3724e-188">Все</span><span class="sxs-lookup"><span data-stu-id="3724e-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-189">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-190">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3724e-191">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-192">До</span><span class="sxs-lookup"><span data-stu-id="3724e-192">Before</span></span></td>
<td><span data-ttu-id="3724e-193">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-194">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-195">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3724e-196">После</span><span class="sxs-lookup"><span data-stu-id="3724e-196">After</span></span></td>
<td><span data-ttu-id="3724e-197">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-198">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3724e-199">Карантин</span><span class="sxs-lookup"><span data-stu-id="3724e-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-200">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3724e-201">До</span><span class="sxs-lookup"><span data-stu-id="3724e-201">Before</span></span></td>
<td><span data-ttu-id="3724e-202">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-203">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-204">После</span><span class="sxs-lookup"><span data-stu-id="3724e-204">After</span></span></td>
<td><span data-ttu-id="3724e-205">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-206">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-206">End</span></span></td>
<td><span data-ttu-id="3724e-207">До</span><span class="sxs-lookup"><span data-stu-id="3724e-207">Before</span></span></td>
<td><span data-ttu-id="3724e-208">Конец</span><span class="sxs-lookup"><span data-stu-id="3724e-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3724e-209">Операция маршрута</span><span class="sxs-lookup"><span data-stu-id="3724e-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-210">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3724e-211">До</span><span class="sxs-lookup"><span data-stu-id="3724e-211">Before</span></span></td>
<td><span data-ttu-id="3724e-212">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-213">Определенный код, группа или специфичный для ресурса, группа или все</span><span class="sxs-lookup"><span data-stu-id="3724e-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-214">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-215">После</span><span class="sxs-lookup"><span data-stu-id="3724e-215">After</span></span></td>
<td><span data-ttu-id="3724e-216">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3724e-217">Производство сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="3724e-217">Co-product production</span></span></td>
<td><span data-ttu-id="3724e-218">Регистрация</span><span class="sxs-lookup"><span data-stu-id="3724e-218">Registration</span></span></td>
<td><span data-ttu-id="3724e-219">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3724e-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-220">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3724e-221">Все</span><span class="sxs-lookup"><span data-stu-id="3724e-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3724e-222">Приемка</span><span class="sxs-lookup"><span data-stu-id="3724e-222">Report as finished</span></span></td>
<td><span data-ttu-id="3724e-223">До</span><span class="sxs-lookup"><span data-stu-id="3724e-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-224">После</span><span class="sxs-lookup"><span data-stu-id="3724e-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3724e-225">В таблице ниже приведены дополнительные сведения о том, как формируются заказы для определенных типов процессов.</span><span class="sxs-lookup"><span data-stu-id="3724e-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="3724e-226">Тип процесса</span><span class="sxs-lookup"><span data-stu-id="3724e-226">Type of process</span></span></th>
<th><span data-ttu-id="3724e-227">Когда можно автоматически формировать заказы по контролю качества</span><span class="sxs-lookup"><span data-stu-id="3724e-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="3724e-228">Когда можно формировать заказа, если применяются разрушающие испытания</span><span class="sxs-lookup"><span data-stu-id="3724e-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="3724e-229">Описание условия</span><span class="sxs-lookup"><span data-stu-id="3724e-229">Condition information</span></span></th>
<th><span data-ttu-id="3724e-230">Сведения о ручном формировании</span><span class="sxs-lookup"><span data-stu-id="3724e-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3724e-231">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="3724e-231">Purchase order</span></span></td>
<td><span data-ttu-id="3724e-232">До или после разноски поступления продуктов получаемого материала</span><span class="sxs-lookup"><span data-stu-id="3724e-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="3724e-233">После разноски отборочной накладной на полученные материалы, поскольку материалы должны быть доступны для проведения испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="3724e-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="3724e-234">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3724e-235">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="3724e-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-236">Карантинный заказ</span><span class="sxs-lookup"><span data-stu-id="3724e-236">Quarantine order</span></span></td>
<td><span data-ttu-id="3724e-237">До или после завершения карантинного заказа</span><span class="sxs-lookup"><span data-stu-id="3724e-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="3724e-238">Нельзя формировать заказы с разрушительными испытаниями.</span><span class="sxs-lookup"><span data-stu-id="3724e-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="3724e-239">Предполагается, что функции карантинного заказа учитывают разрушаемые материалы.</span><span class="sxs-lookup"><span data-stu-id="3724e-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="3724e-240">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3724e-241">Созданный вручную качественный заказ, относящийся к карантинному заказу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="3724e-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-242">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="3724e-242">Sales order</span></span></td>
<td><span data-ttu-id="3724e-243">Перед обновлением запланированного процесса комплектации или отборочной накладной для отгружаемых номенклатур</span><span class="sxs-lookup"><span data-stu-id="3724e-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="3724e-244">В любом шаге</span><span class="sxs-lookup"><span data-stu-id="3724e-244">At any step</span></span></td>
<td><span data-ttu-id="3724e-245">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или заказчика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3724e-246">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="3724e-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-247">Производственный заказ</span><span class="sxs-lookup"><span data-stu-id="3724e-247">Production order</span></span></td>
<td><span data-ttu-id="3724e-248">До или после регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="3724e-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3724e-249">После регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="3724e-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3724e-250">Потребность в заказе на контроль может отражать конкретный объект или номенклатуру, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3724e-251">Созданный вручную качественный заказ, относящийся к производственному заказу может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="3724e-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-252">Производственный заказ с операцией маршрута</span><span class="sxs-lookup"><span data-stu-id="3724e-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="3724e-253">До или после завершения отчета по операции</span><span class="sxs-lookup"><span data-stu-id="3724e-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="3724e-254">После регистрации завершения производства по последней операции</span><span class="sxs-lookup"><span data-stu-id="3724e-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="3724e-255">Потребность в заказе на контроль может отражать конкретный объект, ресурс операции, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="3724e-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3724e-256">Созданный вручную заказ для контроля качества, относящийся к операции маршрута, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="3724e-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3724e-257">Запасы</span><span class="sxs-lookup"><span data-stu-id="3724e-257">Inventory</span></span></td>
<td><span data-ttu-id="3724e-258">Заказ для контроля качества не может быть создан автоматически для проводки в журнале запасов (например, журнал прибылей и убытков или журнал инвентаризации) или для проводок заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="3724e-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3724e-259">Невозможно создать заказ контроля качества для складского количества номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3724e-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="3724e-260">Требуются физические запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="3724e-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="3724e-261">Примеры автоматического создания заказов для контроля качества</span><span class="sxs-lookup"><span data-stu-id="3724e-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="3724e-262">Закупки</span><span class="sxs-lookup"><span data-stu-id="3724e-262">Purchasing</span></span>

<span data-ttu-id="3724e-263">В случае покупки, если для поля **тип события** выбрано **Поступление продуктов** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="3724e-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="3724e-264">Если для параметра **На обновленное количество** указано значение **Да**, заказ контроля качества создается для каждого поступления по заказу на покупку на основе полученного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3724e-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="3724e-265">При каждом получении количества по заказу на покупку создаются новые заказы контроля качества на основе вновь полученного количества.</span><span class="sxs-lookup"><span data-stu-id="3724e-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="3724e-266">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается для первого поступления по заказу на покупку на основе полученного количества.</span><span class="sxs-lookup"><span data-stu-id="3724e-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="3724e-267">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания.</span><span class="sxs-lookup"><span data-stu-id="3724e-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="3724e-268">Заказы для контроля качества не создаются для последующих поступлений по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="3724e-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3724e-269">Спецификация качества</span><span class="sxs-lookup"><span data-stu-id="3724e-269">Quality specification</span></span></th>
<th><span data-ttu-id="3724e-270">На обновленное количество</span><span class="sxs-lookup"><span data-stu-id="3724e-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="3724e-271">На аналитику отслеживания</span><span class="sxs-lookup"><span data-stu-id="3724e-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="3724e-272">Результат</span><span class="sxs-lookup"><span data-stu-id="3724e-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3724e-273">Процент: 10%</span><span class="sxs-lookup"><span data-stu-id="3724e-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="3724e-274">Да</span><span class="sxs-lookup"><span data-stu-id="3724e-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="3724e-275">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-275">Batch number: No</span></span></p>
<p><span data-ttu-id="3724e-276">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-277">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="3724e-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="3724e-278">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="3724e-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3724e-279">Заказ для контроля качества #1 для 3 (10% от 30)</span><span class="sxs-lookup"><span data-stu-id="3724e-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-280">Приемка для 70</span><span class="sxs-lookup"><span data-stu-id="3724e-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="3724e-281">Заказ для контроля качества #2 для 7 (10% от оставшегося количества заказа, что соответствует 70 в этом случае)</span><span class="sxs-lookup"><span data-stu-id="3724e-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-282">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="3724e-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3724e-283">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-283">No</span></span></td>
<td>
<p><span data-ttu-id="3724e-284">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-284">Batch number: No</span></span></p>
<p><span data-ttu-id="3724e-285">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="3724e-286">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="3724e-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="3724e-287">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="3724e-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3724e-288">Заказ для контроля качества #1 создается для 1 (для первого принятого количества, которое имеет фиксированное значение 1).</span><span class="sxs-lookup"><span data-stu-id="3724e-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="3724e-289">Для оставшегося количества заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-290">Приемка для 10</span><span class="sxs-lookup"><span data-stu-id="3724e-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="3724e-291">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-292">Приемка для 60</span><span class="sxs-lookup"><span data-stu-id="3724e-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="3724e-293">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-294">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="3724e-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3724e-295">Да</span><span class="sxs-lookup"><span data-stu-id="3724e-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="3724e-296">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3724e-297">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-298">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="3724e-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3724e-299">Приемка для 3</span><span class="sxs-lookup"><span data-stu-id="3724e-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="3724e-300">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="3724e-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3724e-301">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="3724e-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3724e-302">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="3724e-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-303">Приемка для 2</span><span class="sxs-lookup"><span data-stu-id="3724e-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="3724e-304">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="3724e-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="3724e-305">Заказ для контроля качества #5 для 1 партии #b5, последовательный #s5</span><span class="sxs-lookup"><span data-stu-id="3724e-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="3724e-306"><strong>Примечание:</strong> партия может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="3724e-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-307">Фиксированное количество: 2</span><span class="sxs-lookup"><span data-stu-id="3724e-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="3724e-308">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-308">No</span></span></td>
<td>
<p><span data-ttu-id="3724e-309">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3724e-310">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-311">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="3724e-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3724e-312">Приемка для 4</span><span class="sxs-lookup"><span data-stu-id="3724e-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="3724e-313">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1.</span><span class="sxs-lookup"><span data-stu-id="3724e-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="3724e-314">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2.</span><span class="sxs-lookup"><span data-stu-id="3724e-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="3724e-315">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3.</span><span class="sxs-lookup"><span data-stu-id="3724e-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="3724e-316">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4.</span><span class="sxs-lookup"><span data-stu-id="3724e-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="3724e-317">Для оставшегося количества заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-318">Приемка для 6</span><span class="sxs-lookup"><span data-stu-id="3724e-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="3724e-319">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="3724e-320">Производство</span><span class="sxs-lookup"><span data-stu-id="3724e-320">Production</span></span>

<span data-ttu-id="3724e-321">В случае производства, если для поля **тип события** выбрано **Приемка** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="3724e-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="3724e-322">Если для параметра **На обновленное количество** указано значение **Да**, заказ для контроля качества создается на основе каждого законченного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3724e-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="3724e-323">При каждом принятом количестве в отношении производственный заказа создаются новые заказы для контроля качества на основе нового законченного количества.</span><span class="sxs-lookup"><span data-stu-id="3724e-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="3724e-324">Эта логика создания согласуется с покупкой.</span><span class="sxs-lookup"><span data-stu-id="3724e-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="3724e-325">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается при первом сообщении о том, что количество принято, на основе законченного количества.</span><span class="sxs-lookup"><span data-stu-id="3724e-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="3724e-326">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3724e-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="3724e-327">Заказы для контроля качества не создаются для последующих законченных количеств.</span><span class="sxs-lookup"><span data-stu-id="3724e-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="3724e-328">Спецификация качества</span><span class="sxs-lookup"><span data-stu-id="3724e-328">Quality specification</span></span></th>
<th><span data-ttu-id="3724e-329">На обновленное количество</span><span class="sxs-lookup"><span data-stu-id="3724e-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="3724e-330">На аналитику отслеживания</span><span class="sxs-lookup"><span data-stu-id="3724e-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="3724e-331">Результат</span><span class="sxs-lookup"><span data-stu-id="3724e-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="3724e-332">Процент: 10%</span><span class="sxs-lookup"><span data-stu-id="3724e-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="3724e-333">Да</span><span class="sxs-lookup"><span data-stu-id="3724e-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="3724e-334">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-334">Batch number: No</span></span></p>
<p><span data-ttu-id="3724e-335">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-336">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="3724e-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="3724e-337">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="3724e-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3724e-338">Заказ для контроля качества #1 для 3 (10% от 30)</span><span class="sxs-lookup"><span data-stu-id="3724e-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-339">Приемка для 70</span><span class="sxs-lookup"><span data-stu-id="3724e-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="3724e-340">Заказ для контроля качества #2 для 7 (10% от оставшегося количества заказа, что соответствует 70 в этом случае)</span><span class="sxs-lookup"><span data-stu-id="3724e-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-341">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="3724e-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3724e-342">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-342">No</span></span></td>
<td>
<p><span data-ttu-id="3724e-343">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-343">Batch number: No</span></span></p>
<p><span data-ttu-id="3724e-344">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="3724e-345">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="3724e-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="3724e-346">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="3724e-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3724e-347">Заказ для контроля качества #1 для 1 (для первого принятого количества, которое имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="3724e-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="3724e-348">Заказ для контроля качества #2 для 1 (для оставшегося количества, которое все еще имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="3724e-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-349">Приемка для 10</span><span class="sxs-lookup"><span data-stu-id="3724e-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="3724e-350">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-351">Приемка для 60</span><span class="sxs-lookup"><span data-stu-id="3724e-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="3724e-352">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-353">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="3724e-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3724e-354">Да</span><span class="sxs-lookup"><span data-stu-id="3724e-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="3724e-355">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3724e-356">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-357">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="3724e-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3724e-358">Приемка для 3: 1 для #b1, #s1; 1 для #b2, #s2; и 1 для #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="3724e-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="3724e-359">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="3724e-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3724e-360">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="3724e-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3724e-361">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="3724e-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-362">Приемка для 2: 1 для #b4, #s4; и 1 для #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="3724e-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="3724e-363">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="3724e-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="3724e-364">Заказ для контроля качества #5 для 1 партии #b5, последовательный #s5</span><span class="sxs-lookup"><span data-stu-id="3724e-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="3724e-365"><strong>Примечание:</strong> партия может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="3724e-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3724e-366">Фиксированное количество: 2</span><span class="sxs-lookup"><span data-stu-id="3724e-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="3724e-367">Нет</span><span class="sxs-lookup"><span data-stu-id="3724e-367">No</span></span></td>
<td>
<p><span data-ttu-id="3724e-368">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3724e-369">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="3724e-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3724e-370">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="3724e-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3724e-371">Приемка для 4: 1 для #b1, #s1; 1 для #b2, #s2; 1 для #b3, #s3 и 1 для #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="3724e-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="3724e-372">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="3724e-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="3724e-373">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="3724e-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="3724e-374">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="3724e-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="3724e-375">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="3724e-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="3724e-376">Заказ для контроля качества #5 для 2, без ссылки на партию и серийный номер</span><span class="sxs-lookup"><span data-stu-id="3724e-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3724e-377">Приемка для 6: 1 для #b5, #s5; 1 для #b6, #s6; 1 для #b7, #s7; 1 для #b8, #s8; 1 для #b9, #s9; и 1 для #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="3724e-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="3724e-378">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="3724e-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="3724e-379">Страницы управления качеством</span><span class="sxs-lookup"><span data-stu-id="3724e-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3724e-380">Страница</span><span class="sxs-lookup"><span data-stu-id="3724e-380">Page</span></span></th>
<th><span data-ttu-id="3724e-381">Описание</span><span class="sxs-lookup"><span data-stu-id="3724e-381">Description</span></span></th>
<th><span data-ttu-id="3724e-382">Пример</span><span class="sxs-lookup"><span data-stu-id="3724e-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3724e-383">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="3724e-383">Quality associations</span></span></td>
<td><span data-ttu-id="3724e-384">См. предыдущие разделы этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3724e-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="3724e-385">Ассоциация качества определяет всю следующую информацию для созданного заказа для контроля качества:</span><span class="sxs-lookup"><span data-stu-id="3724e-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="3724e-386">Событие проводки</span><span class="sxs-lookup"><span data-stu-id="3724e-386">The transaction event</span></span></li>
<li><span data-ttu-id="3724e-387">Набор проверок, которые необходимо выполнить для номенклатур</span><span class="sxs-lookup"><span data-stu-id="3724e-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="3724e-388">Допустимый уровень качества</span><span class="sxs-lookup"><span data-stu-id="3724e-388">The AQL</span></span></li>
<li><span data-ttu-id="3724e-389">План выборочного контроля</span><span class="sxs-lookup"><span data-stu-id="3724e-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="3724e-390">Необходимо определить сопоставление контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="3724e-391">Например, заказ для контроля качества может создаваться в бизнес-процессах для заказов на покупку, карантинных заказов, заказов на продажу и производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="3724e-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3724e-392">Тесты</span><span class="sxs-lookup"><span data-stu-id="3724e-392">Tests</span></span></td>
<td><span data-ttu-id="3724e-393">Эта страница используется для назначения и просмотра отдельных испытаний, определяющих соответствие вашей продукции требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="3724e-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="3724e-394">Вы можете назначить одни или несколько индивидуальных испытаний в группе проверки.</span><span class="sxs-lookup"><span data-stu-id="3724e-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="3724e-395">В этом случае вы также определяете информацию, специфичную для теста, такую как приемлемые значения измерения.</span><span class="sxs-lookup"><span data-stu-id="3724e-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="3724e-396">Значения измерения используются для испытаний с количественными результатами, и переменные испытания используются для качественных испытаний.</span><span class="sxs-lookup"><span data-stu-id="3724e-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="3724e-397">Количественное испытание имеет тип испытания <strong>Целое число</strong> или <strong>Дробь</strong>, и также имеет обозначенную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="3724e-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="3724e-398">Спецификации качества и результаты теста выражаются числами.</span><span class="sxs-lookup"><span data-stu-id="3724e-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="3724e-399">Качественное испытание имеет тип проверки <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="3724e-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="3724e-400">Для качественных испытаний требуется дополнительная информация об измеряемой тестовой переменной и ее возможных перечислимых вариантах.</span><span class="sxs-lookup"><span data-stu-id="3724e-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="3724e-401">Спецификации качества и результаты теста выражаются в соответствии с результатом.</span><span class="sxs-lookup"><span data-stu-id="3724e-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="3724e-402">Производственная компания проводит два испытания купленных материалов: количественное испытание качества материала и качественную проверку повреждения упаковки.</span><span class="sxs-lookup"><span data-stu-id="3724e-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="3724e-403">Компания определяет дополнительную информацию о качественном испытании, чтобы идентифицировать переменную испытания (поврежденная упаковка) и ее результаты.</span><span class="sxs-lookup"><span data-stu-id="3724e-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="3724e-404">Компания использует страницу <strong>Группы проверки</strong> для того, чтобы назначить два испытания в группу проверки и указать информацию, специфичную для испытания.</span><span class="sxs-lookup"><span data-stu-id="3724e-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="3724e-405">Группа испытаний назначается заказу контроля качества, таким образом компания может составить отчет по результатам этих двух испытаний.</span><span class="sxs-lookup"><span data-stu-id="3724e-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3724e-406">Группы проверки</span><span class="sxs-lookup"><span data-stu-id="3724e-406">Test groups</span></span></td>
<td><span data-ttu-id="3724e-407">Эта страница используется для настройки, изменения и просмотра групп проверки и отдельных проверок, включенных в проверочную группу.</span><span class="sxs-lookup"><span data-stu-id="3724e-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="3724e-408">В верхней области отображаются группы испытаний, а в нижней области отображаются испытания, включенные в выбранную группу испытаний.</span><span class="sxs-lookup"><span data-stu-id="3724e-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="3724e-409">Группе испытаний назначаются несколько политик, такие как план выборочного контроля, приемлемый уровень качества и потребности для испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="3724e-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="3724e-410">Когда вы назначаете индивидуальное испытание для контрольной группы, вы определяете дополнительную информацию, такую как последовательность, документы и даты срока действия.</span><span class="sxs-lookup"><span data-stu-id="3724e-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="3724e-411">Для количественного испытания информация, которую вы определяете, также включает приемлемые значения измерений.</span><span class="sxs-lookup"><span data-stu-id="3724e-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="3724e-412">Для качественного испытания информация включает переменную испытания и результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3724e-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="3724e-413">Группа проверок, назначенная заказу на контроль качества, определяет начальный набор испытаний, которые должны выполняться для указанной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3724e-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="3724e-414">Однако можно в заказе для контроля качества можно добавлять, удалять или изменять испытания.</span><span class="sxs-lookup"><span data-stu-id="3724e-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="3724e-415">Результаты проверок указываются для каждой проверки в заказе контроля качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="3724e-416">Производственная компания определяет группу испытаний для каждой разновидности своих инструкций по обеспечению качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="3724e-417">Разные группы испытаний отражают различия планов выборочного контроля, наборов испытаний, которые должны быть выполнены совместно, приемлемых уровней качества, а также других коэффициентов.</span><span class="sxs-lookup"><span data-stu-id="3724e-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="3724e-418">Для испытаний с количественными результатами также имеются различия в приемлемых значениях измерений.</span><span class="sxs-lookup"><span data-stu-id="3724e-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="3724e-419">Чтобы обеспечить принудительное выполнение инструкций по обеспечению качества, компания назначает проверочную группу для каждого правила автоматического создания заказов контроля качества (на странице <strong>Сопоставления контроля качества</strong>), а также назначает проверочную группу создаваемым вручную заказам для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3724e-420">Группы контроля качества номенклатуры</span><span class="sxs-lookup"><span data-stu-id="3724e-420">Item quality groups</span></span></td>
<td><span data-ttu-id="3724e-421">Эта страница используется для настройки, изменения и просмотра номенклатур, назначенных группе контроля качества, или групп контроля качества, назначенных номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="3724e-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="3724e-422">Группа контроля качества определяет общие требования к проверке номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3724e-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="3724e-423">После определения требованиям к испытанию на странице <strong>Группы проверки</strong> вы можете определить правила для автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="3724e-424">Для того, чтобы упростить процесс, вы не определяете правила для индивидуальных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3724e-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="3724e-425">Вместо этого вы определяете правила для группы качества путем использования страницы <strong>Сопоставления контроля качества</strong>.</span><span class="sxs-lookup"><span data-stu-id="3724e-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="3724e-426">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной группы качества, чтобы назначить соответствующие номенклатуры для этой группы.</span><span class="sxs-lookup"><span data-stu-id="3724e-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="3724e-427">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной номенклатуры, чтобы назначить соответствующую группу качества для этой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3724e-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="3724e-428">Производственная компания приобретает различные виды сырья, для которых действуют одинаковые требования по проверке во время входного контроля.</span><span class="sxs-lookup"><span data-stu-id="3724e-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="3724e-429">Компания определяет группу качества, и после этого назначает коды номенклатур, которые связаны с сырьем, для этой группы.</span><span class="sxs-lookup"><span data-stu-id="3724e-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="3724e-430">Позднее компания покупает новый тип сырья, которое имеет такие же требования к испытаниям.</span><span class="sxs-lookup"><span data-stu-id="3724e-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="3724e-431">Вместо настройки новых требований к испытаниям для нового материала компания добавляет код номенклатуры для нового материала к существующей группе качества.</span><span class="sxs-lookup"><span data-stu-id="3724e-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="3724e-432">Эта же производственная компания также производит номенклатуры, которые имеют одинаковые требования в отношении производственных испытаний и одинаковые требования в отношении проведения испытаний перед отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="3724e-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="3724e-433">Компания определяет две дополнительные группы контроля качества и назначает соответствующие коды номенклатур каждой группе.</span><span class="sxs-lookup"><span data-stu-id="3724e-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3724e-434">Переменные проверки</span><span class="sxs-lookup"><span data-stu-id="3724e-434">Test variables</span></span></td>
<td><span data-ttu-id="3724e-435">Используйте эту страницу для определения и просмотра переменных, связанных с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="3724e-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="3724e-436">Для каждой переменной вы определяете перечислимые результаты, которые представляют возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="3724e-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="3724e-437">Вы определяете испытания на странице <strong>Тесты</strong>.</span><span class="sxs-lookup"><span data-stu-id="3724e-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="3724e-438">Для качественных тестов вы должны установить тип испытания <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="3724e-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="3724e-439">Используйте страницу <strong>Группы проверки</strong> для назначения тестовой переменной отдельному тесту.</span><span class="sxs-lookup"><span data-stu-id="3724e-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="3724e-440">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="3724e-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="3724e-441">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="3724e-441">This inspection test has several variables.</span></span> <span data-ttu-id="3724e-442">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="3724e-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="3724e-443">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="3724e-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3724e-444">Результаты переменной проверки</span><span class="sxs-lookup"><span data-stu-id="3724e-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="3724e-445">Используйте эту страницу для настройки, изменения и просмотра возможных результатов испытаний тестовой переменной, связанной с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="3724e-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="3724e-446">Для каждого результата назначается статус <strong>приемлемый</strong> или <strong>неприемлемый</strong>.</span><span class="sxs-lookup"><span data-stu-id="3724e-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="3724e-447">Следует определить переменную и ее результаты для каждого качественного испытания, которое определено на странице <strong>Тесты</strong></span><span class="sxs-lookup"><span data-stu-id="3724e-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="3724e-448">(Для качественных тестов задается тип испытания <strong>Параметры</strong> на странице <strong>Тесты</strong>.) Используйте страницу <strong>Группы проверки</strong>, чтобы назначить тестовую переменную и результат по умолчанию для отдельного качественного испытания.</span><span class="sxs-lookup"><span data-stu-id="3724e-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="3724e-449">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="3724e-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="3724e-450">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="3724e-450">This inspection test has of several variables.</span></span> <span data-ttu-id="3724e-451">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="3724e-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="3724e-452">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="3724e-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="3724e-453">Для каждого результата назначен статус <strong>положительного</strong> или <strong>отрицательного</strong> результата.</span><span class="sxs-lookup"><span data-stu-id="3724e-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="3724e-454">В ходе проверки каждой переменной инспектор создает отчет о результатах, выбирая один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="3724e-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="3724e-455">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3724e-455">Additional resources</span></span>
--------

[<span data-ttu-id="3724e-456">Процессы управления качеством</span><span class="sxs-lookup"><span data-stu-id="3724e-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="3724e-457">Включение управления несоответствиями</span><span class="sxs-lookup"><span data-stu-id="3724e-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
