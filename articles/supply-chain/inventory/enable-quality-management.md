---
title: Обзор управления качеством
description: Эта тема описывает, как можно использовать управление качеством в Dynamics 365 Supply Chain Management, чтобы улучшить качество продукта в вашей цепи поставок.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b090450c6b39607f9661667f8063998bbe5ff52
ms.sourcegitcommit: c79062ba89498aa3fe3d86e478d9f32484f5f6dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "3224917"
---
# <a name="quality-management-overview"></a><span data-ttu-id="b253d-103">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="b253d-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b253d-104">Эта тема описывает, как можно использовать управление качеством в Dynamics 365 Supply Chain Management, чтобы улучшить качество продукта в вашей цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="b253d-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="b253d-105">Управление качеством может помочь вам управлять периодами оборота, когда вы работаете с несоответствующими продуктами, независимо от их источника происхождения.</span><span class="sxs-lookup"><span data-stu-id="b253d-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="b253d-106">Поскольку диагностические типы связаны с отчетностью о коррекции, Supply Chain Management может планировать задачи для исправления проблем и предотвращения их повторения.</span><span class="sxs-lookup"><span data-stu-id="b253d-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="b253d-107">В дополнение к функциональности для управляя несоответствием, управление качеством включает функциональность для отслеживания проблем по типу проблемы (даже внутренние проблемы), и для определения решений как краткосрочные или долгосрочные.</span><span class="sxs-lookup"><span data-stu-id="b253d-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="b253d-108">Статистика по ключевым индикаторам производительности обеспечивает анализ истории предыдущих проблем несоответствия и решений, которые были применены для их исправления.</span><span class="sxs-lookup"><span data-stu-id="b253d-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="b253d-109">Вы можете использовать исторические данные для просмотра эффективности предыдущих мер по обеспечению качества и определить соответствующие меры для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="b253d-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="b253d-110">При указании сопоставления контроля качества Supply Chain Management может сформировать заказы по контролю качества для различных бизнес-процессов, событий и условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="b253d-111">Сопоставление может относиться к определенной номенклатуре, группе или ко всем продуктам.</span><span class="sxs-lookup"><span data-stu-id="b253d-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="b253d-112">Примеры использования управления качеством</span><span class="sxs-lookup"><span data-stu-id="b253d-112">Examples of the use of quality management</span></span>
<span data-ttu-id="b253d-113">Управление качеством гибкое и может быть реализована различными способами для соответствия требованиям определенных уровней операций цепочки снабжения.</span><span class="sxs-lookup"><span data-stu-id="b253d-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="b253d-114">Следующие примеры иллюстрируют возможное использование этих функций.</span><span class="sxs-lookup"><span data-stu-id="b253d-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="b253d-115">Автоматический запуск процесса контроля качества, основанный на предопределенных критериях (после регистрации на складе заказа на покупку от определенного поставщика).</span><span class="sxs-lookup"><span data-stu-id="b253d-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="b253d-116">Блокировка запасов во время проверки для исключения использования неутвержденных запасов (полная блокировка количеств по заказу на покупку).</span><span class="sxs-lookup"><span data-stu-id="b253d-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="b253d-117">Использование выборочного контроля номенклатур в рамках ассоциации качества для того, чтобы определить сумму текущих физических запасов, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="b253d-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="b253d-118">Выборочный контроль может быть основан на фиксированных количествах или на процентном объеме.</span><span class="sxs-lookup"><span data-stu-id="b253d-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="b253d-119">Создайте заказы для контроля качества для частичных приемок.</span><span class="sxs-lookup"><span data-stu-id="b253d-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="b253d-120">Чтобы создать заказ для контроля качества, основанный на количестве, физически полученном с заказом, необходимо установить флажок **На обновленное количество** в форме **Выборка элементов**.</span><span class="sxs-lookup"><span data-stu-id="b253d-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="b253d-121">Создание типов испытаний, которые включают минимальные, максимальные и целевые значения испытаний, и выполнение качественного или количественного тестирования с предопределенными результатами проверки.</span><span class="sxs-lookup"><span data-stu-id="b253d-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="b253d-122">Указание допустимого уровня качества (AQL) для управления допусками измерения качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="b253d-123">Указание ресурсов, которые требуются для контрольной операции, например испытательный участок и инструменты для испытаний.</span><span class="sxs-lookup"><span data-stu-id="b253d-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="b253d-124">Работа с сопоставлениями контроля качества</span><span class="sxs-lookup"><span data-stu-id="b253d-124">Working with quality associations</span></span>
<span data-ttu-id="b253d-125">Бизнес-процесс, использующий сопоставления, может быть связан с различными исходными документами, такими как заказы на покупку, заказы на продажу и производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="b253d-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="b253d-126">Каждая запись сопоставления качества определяет также набор тестов, AQL и план выборочного контроля, применимые для создаваемых автоматически качественных заказов.</span><span class="sxs-lookup"><span data-stu-id="b253d-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="b253d-127">Необходимо определить запись сопоставления контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="b253d-128">Например, можно создать сопоставление, которое формирует заказ контроля качества для заказов на продажу, когда обновляется поступление продуктов по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="b253d-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="b253d-129">В зависимости от настройки плана исполнения возможна блокировка самого запускающего процесса, пока имеется открытый заказ для контроля качества, или блокировка следующих процессов, таких как выставление накладной по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="b253d-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="b253d-130">**Примечание.** Пока имеются открытые заказы для контроля качества, количества запасов автоматически блокируются по выдаче.</span><span class="sxs-lookup"><span data-stu-id="b253d-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="b253d-131">В зависимости от настройки **Полная блокировка** на странице **Выборка номенклатур**, количество равно количеству в заказе для контроля качества или количеству в строке исходного документа.</span><span class="sxs-lookup"><span data-stu-id="b253d-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="b253d-132">Сопоставление по контролю качестве указывает событие и условия, при которых формируется заказ на контроль качества для определенного бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="b253d-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="b253d-133">Условия могут быть заданы для определенного места или юридического лица.</span><span class="sxs-lookup"><span data-stu-id="b253d-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="b253d-134">Заказ по контролю качества, в котором используются разрушающие испытания, может формироваться, только если для данного события имеется складской запас.</span><span class="sxs-lookup"><span data-stu-id="b253d-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="b253d-135">Следующие примеры иллюстрируют определение записи сопоставления качества для отклонений в бизнес-процессах.</span><span class="sxs-lookup"><span data-stu-id="b253d-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="b253d-136">Примеры обобщаются также в следующей таблице в плане событий и условий, определенных записью сопоставления качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b253d-137">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="b253d-137">Reference type</span></span></th>
<th><span data-ttu-id="b253d-138">Тип события</span><span class="sxs-lookup"><span data-stu-id="b253d-138">Event type</span></span></th>
<th><span data-ttu-id="b253d-139">Выполнение</span><span class="sxs-lookup"><span data-stu-id="b253d-139">Execution</span></span></th>
<th><span data-ttu-id="b253d-140">Блокировка событий</span><span class="sxs-lookup"><span data-stu-id="b253d-140">Event blocking</span></span></th>
<th><span data-ttu-id="b253d-141">Ссылка на документ</span><span class="sxs-lookup"><span data-stu-id="b253d-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b253d-142">Запасы</span><span class="sxs-lookup"><span data-stu-id="b253d-142">Inventory</span></span></td>
<td><span data-ttu-id="b253d-143">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b253d-143">Not applicable</span></span></td>
<td><span data-ttu-id="b253d-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b253d-144">Not applicable</span></span></td>
<td><span data-ttu-id="b253d-145">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-145">None</span></span></td>
<td><span data-ttu-id="b253d-146">Все</span><span class="sxs-lookup"><span data-stu-id="b253d-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="b253d-147">Прод.</span><span class="sxs-lookup"><span data-stu-id="b253d-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="b253d-148">Процесс комплектации запланирован</span><span class="sxs-lookup"><span data-stu-id="b253d-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="b253d-149">До</span><span class="sxs-lookup"><span data-stu-id="b253d-149">Before</span></span></td>
<td><span data-ttu-id="b253d-150">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="b253d-151">Только определенный код, группа или все</span><span class="sxs-lookup"><span data-stu-id="b253d-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-152">Процесс комплектации</span><span class="sxs-lookup"><span data-stu-id="b253d-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-153">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="b253d-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-154">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b253d-155">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="b253d-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-156">До</span><span class="sxs-lookup"><span data-stu-id="b253d-156">Before</span></span></td>
<td><span data-ttu-id="b253d-157">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-158">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="b253d-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-159">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="b253d-160">Покупка</span><span class="sxs-lookup"><span data-stu-id="b253d-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="b253d-161">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="b253d-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="b253d-162">До</span><span class="sxs-lookup"><span data-stu-id="b253d-162">Before</span></span></td>
<td><span data-ttu-id="b253d-163">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-164">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="b253d-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-165">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-166">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b253d-167">После</span><span class="sxs-lookup"><span data-stu-id="b253d-167">After</span></span></td>
<td><span data-ttu-id="b253d-168">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-169">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-170">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b253d-171">Регистрация</span><span class="sxs-lookup"><span data-stu-id="b253d-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-172">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b253d-172">Not applicable</span></span></td>
<td><span data-ttu-id="b253d-173">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-174">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-175">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b253d-176">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-177">До</span><span class="sxs-lookup"><span data-stu-id="b253d-177">Before</span></span></td>
<td><span data-ttu-id="b253d-178">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-179">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-180">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b253d-181">После</span><span class="sxs-lookup"><span data-stu-id="b253d-181">After</span></span></td>
<td><span data-ttu-id="b253d-182">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-183">Счет</span><span class="sxs-lookup"><span data-stu-id="b253d-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="b253d-184">Производство</span><span class="sxs-lookup"><span data-stu-id="b253d-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-185">Регистрация</span><span class="sxs-lookup"><span data-stu-id="b253d-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-186">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b253d-186">Not applicable</span></span></td>
<td><span data-ttu-id="b253d-187">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="b253d-188">Все</span><span class="sxs-lookup"><span data-stu-id="b253d-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-189">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-190">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b253d-191">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-192">До</span><span class="sxs-lookup"><span data-stu-id="b253d-192">Before</span></span></td>
<td><span data-ttu-id="b253d-193">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-194">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-195">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b253d-196">После</span><span class="sxs-lookup"><span data-stu-id="b253d-196">After</span></span></td>
<td><span data-ttu-id="b253d-197">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-198">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b253d-199">Карантин</span><span class="sxs-lookup"><span data-stu-id="b253d-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-200">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b253d-201">До</span><span class="sxs-lookup"><span data-stu-id="b253d-201">Before</span></span></td>
<td><span data-ttu-id="b253d-202">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-203">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-204">После</span><span class="sxs-lookup"><span data-stu-id="b253d-204">After</span></span></td>
<td><span data-ttu-id="b253d-205">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-206">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-206">End</span></span></td>
<td><span data-ttu-id="b253d-207">До</span><span class="sxs-lookup"><span data-stu-id="b253d-207">Before</span></span></td>
<td><span data-ttu-id="b253d-208">Конец</span><span class="sxs-lookup"><span data-stu-id="b253d-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b253d-209">Операция маршрута</span><span class="sxs-lookup"><span data-stu-id="b253d-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-210">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b253d-211">До</span><span class="sxs-lookup"><span data-stu-id="b253d-211">Before</span></span></td>
<td><span data-ttu-id="b253d-212">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-213">Определенный код, группа или специфичный для ресурса, группа или все</span><span class="sxs-lookup"><span data-stu-id="b253d-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-214">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-215">После</span><span class="sxs-lookup"><span data-stu-id="b253d-215">After</span></span></td>
<td><span data-ttu-id="b253d-216">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b253d-217">Производство сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="b253d-217">Co-product production</span></span></td>
<td><span data-ttu-id="b253d-218">Регистрация</span><span class="sxs-lookup"><span data-stu-id="b253d-218">Registration</span></span></td>
<td><span data-ttu-id="b253d-219">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="b253d-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-220">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b253d-221">Все</span><span class="sxs-lookup"><span data-stu-id="b253d-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b253d-222">Приемка</span><span class="sxs-lookup"><span data-stu-id="b253d-222">Report as finished</span></span></td>
<td><span data-ttu-id="b253d-223">До</span><span class="sxs-lookup"><span data-stu-id="b253d-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-224">После</span><span class="sxs-lookup"><span data-stu-id="b253d-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b253d-225">В таблице ниже приведены дополнительные сведения о том, как формируются заказы для определенных типов процессов.</span><span class="sxs-lookup"><span data-stu-id="b253d-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="b253d-226">Тип процесса</span><span class="sxs-lookup"><span data-stu-id="b253d-226">Type of process</span></span></th>
<th><span data-ttu-id="b253d-227">Когда можно автоматически формировать заказы по контролю качества</span><span class="sxs-lookup"><span data-stu-id="b253d-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="b253d-228">Когда можно формировать заказа, если применяются разрушающие испытания</span><span class="sxs-lookup"><span data-stu-id="b253d-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="b253d-229">Описание условия</span><span class="sxs-lookup"><span data-stu-id="b253d-229">Condition information</span></span></th>
<th><span data-ttu-id="b253d-230">Сведения о ручном формировании</span><span class="sxs-lookup"><span data-stu-id="b253d-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b253d-231">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="b253d-231">Purchase order</span></span></td>
<td><span data-ttu-id="b253d-232">До или после разноски поступления продуктов получаемого материала</span><span class="sxs-lookup"><span data-stu-id="b253d-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="b253d-233">После разноски отборочной накладной на полученные материалы, поскольку материалы должны быть доступны для проведения испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="b253d-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="b253d-234">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b253d-235">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="b253d-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-236">Карантинный заказ</span><span class="sxs-lookup"><span data-stu-id="b253d-236">Quarantine order</span></span></td>
<td><span data-ttu-id="b253d-237">До или после завершения карантинного заказа</span><span class="sxs-lookup"><span data-stu-id="b253d-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="b253d-238">Нельзя формировать заказы с разрушительными испытаниями.</span><span class="sxs-lookup"><span data-stu-id="b253d-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="b253d-239">Предполагается, что функции карантинного заказа учитывают разрушаемые материалы.</span><span class="sxs-lookup"><span data-stu-id="b253d-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="b253d-240">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b253d-241">Созданный вручную качественный заказ, относящийся к карантинному заказу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="b253d-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-242">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="b253d-242">Sales order</span></span></td>
<td><span data-ttu-id="b253d-243">Перед обновлением запланированного процесса комплектации или отборочной накладной для отгружаемых номенклатур</span><span class="sxs-lookup"><span data-stu-id="b253d-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="b253d-244">В любом шаге</span><span class="sxs-lookup"><span data-stu-id="b253d-244">At any step</span></span></td>
<td><span data-ttu-id="b253d-245">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или заказчика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b253d-246">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="b253d-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-247">Производственный заказ</span><span class="sxs-lookup"><span data-stu-id="b253d-247">Production order</span></span></td>
<td><span data-ttu-id="b253d-248">До или после регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="b253d-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b253d-249">После регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="b253d-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b253d-250">Потребность в заказе на контроль может отражать конкретный объект или номенклатуру, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b253d-251">Созданный вручную качественный заказ, относящийся к производственному заказу может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="b253d-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-252">Производственный заказ с операцией маршрута</span><span class="sxs-lookup"><span data-stu-id="b253d-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="b253d-253">До или после завершения отчета по операции</span><span class="sxs-lookup"><span data-stu-id="b253d-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="b253d-254">После регистрации завершения производства по последней операции</span><span class="sxs-lookup"><span data-stu-id="b253d-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="b253d-255">Потребность в заказе на контроль может отражать конкретный объект, ресурс операции, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="b253d-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b253d-256">Созданный вручную заказ для контроля качества, относящийся к операции маршрута, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="b253d-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b253d-257">Запасы</span><span class="sxs-lookup"><span data-stu-id="b253d-257">Inventory</span></span></td>
<td><span data-ttu-id="b253d-258">Заказ для контроля качества не может быть создан автоматически для проводки в журнале запасов (например, журнал прибылей и убытков или журнал инвентаризации) или для проводок заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="b253d-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b253d-259">Невозможно создать заказ контроля качества для складского количества номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b253d-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="b253d-260">Требуются физические запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="b253d-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="b253d-261">Примеры автоматического создания заказов для контроля качества</span><span class="sxs-lookup"><span data-stu-id="b253d-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="b253d-262">Закупки</span><span class="sxs-lookup"><span data-stu-id="b253d-262">Purchasing</span></span>

<span data-ttu-id="b253d-263">В случае покупки, если для поля **тип события** выбрано **Поступление продуктов** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="b253d-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="b253d-264">Если для параметра **На обновленное количество** указано значение **Да**, заказ контроля качества создается для каждого поступления по заказу на покупку на основе полученного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b253d-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="b253d-265">При каждом получении количества по заказу на покупку создаются новые заказы контроля качества на основе вновь полученного количества.</span><span class="sxs-lookup"><span data-stu-id="b253d-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="b253d-266">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается для первого поступления по заказу на покупку на основе полученного количества.</span><span class="sxs-lookup"><span data-stu-id="b253d-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="b253d-267">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания.</span><span class="sxs-lookup"><span data-stu-id="b253d-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="b253d-268">Заказы для контроля качества не создаются для последующих поступлений по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="b253d-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="b253d-269">Рабочий</span><span class="sxs-lookup"><span data-stu-id="b253d-269">Production</span></span>

<span data-ttu-id="b253d-270">В случае производства, если для поля **тип события** выбрано **Приемка** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="b253d-270">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="b253d-271">Если для параметра **На обновленное количество** указано значение **Да**, заказ для контроля качества создается на основе каждого законченного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b253d-271">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="b253d-272">При каждом принятом количестве в отношении производственный заказа создаются новые заказы для контроля качества на основе нового законченного количества.</span><span class="sxs-lookup"><span data-stu-id="b253d-272">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="b253d-273">Эта логика создания согласуется с покупкой.</span><span class="sxs-lookup"><span data-stu-id="b253d-273">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="b253d-274">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается при первом сообщении о том, что количество принято, на основе законченного количества.</span><span class="sxs-lookup"><span data-stu-id="b253d-274">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="b253d-275">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b253d-275">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="b253d-276">Заказы для контроля качества не создаются для последующих законченных количеств.</span><span class="sxs-lookup"><span data-stu-id="b253d-276">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b253d-277">Спецификация качества</span><span class="sxs-lookup"><span data-stu-id="b253d-277">Quality specification</span></span></th>
<th><span data-ttu-id="b253d-278">На обновленное количество</span><span class="sxs-lookup"><span data-stu-id="b253d-278">Per updated quantity</span></span></th>
<th><span data-ttu-id="b253d-279">На аналитику отслеживания</span><span class="sxs-lookup"><span data-stu-id="b253d-279">Per tracking dimension</span></span></th>
<th><span data-ttu-id="b253d-280">Результат</span><span class="sxs-lookup"><span data-stu-id="b253d-280">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b253d-281">Процент: 10%</span><span class="sxs-lookup"><span data-stu-id="b253d-281">Percentage: 10%</span></span></td>
<td><span data-ttu-id="b253d-282">Да</span><span class="sxs-lookup"><span data-stu-id="b253d-282">Yes</span></span></td>
<td>
<p><span data-ttu-id="b253d-283">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-283">Batch number: No</span></span></p>
<p><span data-ttu-id="b253d-284">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-284">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="b253d-285">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="b253d-285">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="b253d-286">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="b253d-286">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b253d-287">Заказ для контроля качества #1 для 3 (10% от 30)</span><span class="sxs-lookup"><span data-stu-id="b253d-287">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b253d-288">Приемка для 70</span><span class="sxs-lookup"><span data-stu-id="b253d-288">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="b253d-289">Заказ для контроля качества #2 для 7 (10% от оставшегося количества заказа, что соответствует 70 в этом случае)</span><span class="sxs-lookup"><span data-stu-id="b253d-289">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b253d-290">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="b253d-290">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b253d-291">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-291">No</span></span></td>
<td>
<p><span data-ttu-id="b253d-292">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-292">Batch number: No</span></span></p>
<p><span data-ttu-id="b253d-293">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-293">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="b253d-294">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="b253d-294">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="b253d-295">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="b253d-295">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b253d-296">Заказ для контроля качества #1 для 1 (для первого принятого количества, которое имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="b253d-296">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="b253d-297">Заказ для контроля качества #2 для 1 (для оставшегося количества, которое все еще имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="b253d-297">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b253d-298">Приемка для 10</span><span class="sxs-lookup"><span data-stu-id="b253d-298">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="b253d-299">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="b253d-299">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b253d-300">Приемка для 60</span><span class="sxs-lookup"><span data-stu-id="b253d-300">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="b253d-301">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="b253d-301">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b253d-302">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="b253d-302">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b253d-303">Да</span><span class="sxs-lookup"><span data-stu-id="b253d-303">Yes</span></span></td>
<td>
<p><span data-ttu-id="b253d-304">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="b253d-304">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b253d-305">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="b253d-305">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b253d-306">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="b253d-306">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b253d-307">Приемка для 3: 1 для #b1, #s1; 1 для #b2, #s2; и 1 для #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="b253d-307">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="b253d-308">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="b253d-308">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b253d-309">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="b253d-309">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b253d-310">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="b253d-310">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b253d-311">Приемка для 2: 1 для #b4, #s4; и 1 для #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="b253d-311">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="b253d-312">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="b253d-312">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="b253d-313">Заказ для контроля качества #5 для 1 партии #b5, последовательный #s5</span><span class="sxs-lookup"><span data-stu-id="b253d-313">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="b253d-314"><strong>Примечание:</strong> партия может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="b253d-314"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="b253d-315">Фиксированное количество: 2</span><span class="sxs-lookup"><span data-stu-id="b253d-315">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="b253d-316">Нет</span><span class="sxs-lookup"><span data-stu-id="b253d-316">No</span></span></td>
<td>
<p><span data-ttu-id="b253d-317">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="b253d-317">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b253d-318">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="b253d-318">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b253d-319">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="b253d-319">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b253d-320">Приемка для 4: 1 для #b1, #s1; 1 для #b2, #s2; 1 для #b3, #s3 и 1 для #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="b253d-320">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="b253d-321">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="b253d-321">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b253d-322">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="b253d-322">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b253d-323">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="b253d-323">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="b253d-324">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="b253d-324">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="b253d-325">Заказ для контроля качества #5 для 2, без ссылки на партию и серийный номер</span><span class="sxs-lookup"><span data-stu-id="b253d-325">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b253d-326">Приемка для 6: 1 для #b5, #s5; 1 для #b6, #s6; 1 для #b7, #s7; 1 для #b8, #s8; 1 для #b9, #s9; и 1 для #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="b253d-326">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="b253d-327">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="b253d-327">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="b253d-328">Страницы управления качеством</span><span class="sxs-lookup"><span data-stu-id="b253d-328">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b253d-329">Страница</span><span class="sxs-lookup"><span data-stu-id="b253d-329">Page</span></span></th>
<th><span data-ttu-id="b253d-330">Описание</span><span class="sxs-lookup"><span data-stu-id="b253d-330">Description</span></span></th>
<th><span data-ttu-id="b253d-331">Пример</span><span class="sxs-lookup"><span data-stu-id="b253d-331">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b253d-332">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="b253d-332">Quality associations</span></span></td>
<td><span data-ttu-id="b253d-333">См. предыдущие разделы этой статьи.</span><span class="sxs-lookup"><span data-stu-id="b253d-333">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="b253d-334">Ассоциация качества определяет всю следующую информацию для созданного заказа для контроля качества:</span><span class="sxs-lookup"><span data-stu-id="b253d-334">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="b253d-335">Событие проводки</span><span class="sxs-lookup"><span data-stu-id="b253d-335">The transaction event</span></span></li>
<li><span data-ttu-id="b253d-336">Набор проверок, которые необходимо выполнить для номенклатур</span><span class="sxs-lookup"><span data-stu-id="b253d-336">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="b253d-337">Допустимый уровень качества</span><span class="sxs-lookup"><span data-stu-id="b253d-337">The AQL</span></span></li>
<li><span data-ttu-id="b253d-338">План выборочного контроля</span><span class="sxs-lookup"><span data-stu-id="b253d-338">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="b253d-339">Необходимо определить сопоставление контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-339">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="b253d-340">Например, заказ для контроля качества может создаваться в бизнес-процессах для заказов на покупку, карантинных заказов, заказов на продажу и производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="b253d-340">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b253d-341">Тесты</span><span class="sxs-lookup"><span data-stu-id="b253d-341">Tests</span></span></td>
<td><span data-ttu-id="b253d-342">Эта страница используется для назначения и просмотра отдельных испытаний, определяющих соответствие вашей продукции требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="b253d-342">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="b253d-343">Вы можете назначить одни или несколько индивидуальных испытаний в группе проверки.</span><span class="sxs-lookup"><span data-stu-id="b253d-343">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="b253d-344">В этом случае вы также определяете информацию, специфичную для теста, такую как приемлемые значения измерения.</span><span class="sxs-lookup"><span data-stu-id="b253d-344">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="b253d-345">Значения измерения используются для испытаний с количественными результатами, и переменные испытания используются для качественных испытаний.</span><span class="sxs-lookup"><span data-stu-id="b253d-345">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="b253d-346">Количественное испытание имеет тип испытания <strong>Целое число</strong> или <strong>Дробь</strong>, и также имеет обозначенную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="b253d-346">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="b253d-347">Спецификации качества и результаты теста выражаются числами.</span><span class="sxs-lookup"><span data-stu-id="b253d-347">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="b253d-348">Качественное испытание имеет тип проверки <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="b253d-348">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="b253d-349">Для качественных испытаний требуется дополнительная информация об измеряемой тестовой переменной и ее возможных перечислимых вариантах.</span><span class="sxs-lookup"><span data-stu-id="b253d-349">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="b253d-350">Спецификации качества и результаты теста выражаются в соответствии с результатом.</span><span class="sxs-lookup"><span data-stu-id="b253d-350">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="b253d-351">Производственная компания проводит два испытания купленных материалов: количественное испытание качества материала и качественную проверку повреждения упаковки.</span><span class="sxs-lookup"><span data-stu-id="b253d-351">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="b253d-352">Компания определяет дополнительную информацию о качественном испытании, чтобы идентифицировать переменную испытания (поврежденная упаковка) и ее результаты.</span><span class="sxs-lookup"><span data-stu-id="b253d-352">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="b253d-353">Компания использует страницу <strong>Группы проверки</strong> для того, чтобы назначить два испытания в группу проверки и указать информацию, специфичную для испытания.</span><span class="sxs-lookup"><span data-stu-id="b253d-353">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="b253d-354">Группа испытаний назначается заказу контроля качества, таким образом компания может составить отчет по результатам этих двух испытаний.</span><span class="sxs-lookup"><span data-stu-id="b253d-354">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b253d-355">Группы проверки</span><span class="sxs-lookup"><span data-stu-id="b253d-355">Test groups</span></span></td>
<td><span data-ttu-id="b253d-356">Эта страница используется для настройки, изменения и просмотра групп проверки и отдельных проверок, включенных в проверочную группу.</span><span class="sxs-lookup"><span data-stu-id="b253d-356">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="b253d-357">В верхней области отображаются группы испытаний, а в нижней области отображаются испытания, включенные в выбранную группу испытаний.</span><span class="sxs-lookup"><span data-stu-id="b253d-357">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="b253d-358">Группе испытаний назначаются несколько политик, такие как план выборочного контроля, приемлемый уровень качества и потребности для испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="b253d-358">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="b253d-359">Когда вы назначаете индивидуальное испытание для контрольной группы, вы определяете дополнительную информацию, такую как последовательность, документы и даты срока действия.</span><span class="sxs-lookup"><span data-stu-id="b253d-359">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="b253d-360">Для количественного испытания информация, которую вы определяете, также включает приемлемые значения измерений.</span><span class="sxs-lookup"><span data-stu-id="b253d-360">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="b253d-361">Для качественного испытания информация включает переменную испытания и результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b253d-361">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="b253d-362">Группа проверок, назначенная заказу на контроль качества, определяет начальный набор испытаний, которые должны выполняться для указанной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b253d-362">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="b253d-363">Однако можно в заказе для контроля качества можно добавлять, удалять или изменять испытания.</span><span class="sxs-lookup"><span data-stu-id="b253d-363">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="b253d-364">Результаты проверок указываются для каждой проверки в заказе контроля качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-364">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="b253d-365">Производственная компания определяет группу испытаний для каждой разновидности своих инструкций по обеспечению качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-365">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="b253d-366">Разные группы испытаний отражают различия планов выборочного контроля, наборов испытаний, которые должны быть выполнены совместно, приемлемых уровней качества, а также других коэффициентов.</span><span class="sxs-lookup"><span data-stu-id="b253d-366">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="b253d-367">Для испытаний с количественными результатами также имеются различия в приемлемых значениях измерений.</span><span class="sxs-lookup"><span data-stu-id="b253d-367">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="b253d-368">Чтобы обеспечить принудительное выполнение инструкций по обеспечению качества, компания назначает проверочную группу для каждого правила автоматического создания заказов контроля качества (на странице <strong>Сопоставления контроля качества</strong>), а также назначает проверочную группу создаваемым вручную заказам для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-368">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b253d-369">Группы контроля качества номенклатуры</span><span class="sxs-lookup"><span data-stu-id="b253d-369">Item quality groups</span></span></td>
<td><span data-ttu-id="b253d-370">Эта страница используется для настройки, изменения и просмотра номенклатур, назначенных группе контроля качества, или групп контроля качества, назначенных номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="b253d-370">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="b253d-371">Группа контроля качества определяет общие требования к проверке номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b253d-371">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b253d-372">После определения требованиям к испытанию на странице <strong>Группы проверки</strong> вы можете определить правила для автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-372">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b253d-373">Для того, чтобы упростить процесс, вы не определяете правила для индивидуальных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b253d-373">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="b253d-374">Вместо этого вы определяете правила для группы качества путем использования страницы <strong>Сопоставления контроля качества</strong>.</span><span class="sxs-lookup"><span data-stu-id="b253d-374">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="b253d-375">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной группы качества, чтобы назначить соответствующие номенклатуры для этой группы.</span><span class="sxs-lookup"><span data-stu-id="b253d-375">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="b253d-376">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной номенклатуры, чтобы назначить соответствующую группу качества для этой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b253d-376">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="b253d-377">Производственная компания приобретает различные виды сырья, для которых действуют одинаковые требования по проверке во время входного контроля.</span><span class="sxs-lookup"><span data-stu-id="b253d-377">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b253d-378">Компания определяет группу качества, и после этого назначает коды номенклатур, которые связаны с сырьем, для этой группы.</span><span class="sxs-lookup"><span data-stu-id="b253d-378">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b253d-379">Позднее компания покупает новый тип сырья, которое имеет такие же требования к испытаниям.</span><span class="sxs-lookup"><span data-stu-id="b253d-379">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b253d-380">Вместо настройки новых требований к испытаниям для нового материала компания добавляет код номенклатуры для нового материала к существующей группе качества.</span><span class="sxs-lookup"><span data-stu-id="b253d-380">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="b253d-381">Эта же производственная компания также производит номенклатуры, которые имеют одинаковые требования в отношении производственных испытаний и одинаковые требования в отношении проведения испытаний перед отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="b253d-381">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b253d-382">Компания определяет две дополнительные группы контроля качества и назначает соответствующие коды номенклатур каждой группе.</span><span class="sxs-lookup"><span data-stu-id="b253d-382">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b253d-383">Переменные проверки</span><span class="sxs-lookup"><span data-stu-id="b253d-383">Test variables</span></span></td>
<td><span data-ttu-id="b253d-384">Используйте эту страницу для определения и просмотра переменных, связанных с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="b253d-384">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="b253d-385">Для каждой переменной вы определяете перечислимые результаты, которые представляют возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="b253d-385">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="b253d-386">Вы определяете испытания на странице <strong>Тесты</strong>.</span><span class="sxs-lookup"><span data-stu-id="b253d-386">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b253d-387">Для качественных тестов вы должны установить тип испытания <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="b253d-387">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="b253d-388">Используйте страницу <strong>Группы проверки</strong> для назначения тестовой переменной отдельному тесту.</span><span class="sxs-lookup"><span data-stu-id="b253d-388">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="b253d-389">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="b253d-389">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b253d-390">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="b253d-390">This inspection test has several variables.</span></span> <span data-ttu-id="b253d-391">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="b253d-391">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b253d-392">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="b253d-392">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b253d-393">Результаты переменной проверки</span><span class="sxs-lookup"><span data-stu-id="b253d-393">Test variable outcomes</span></span></td>
<td><span data-ttu-id="b253d-394">Используйте эту страницу для настройки, изменения и просмотра возможных результатов испытаний тестовой переменной, связанной с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="b253d-394">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="b253d-395">Для каждого результата назначается статус <strong>приемлемый</strong> или <strong>неприемлемый</strong>.</span><span class="sxs-lookup"><span data-stu-id="b253d-395">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="b253d-396">Следует определить переменную и ее результаты для каждого качественного испытания, которое определено на странице <strong>Тесты</strong></span><span class="sxs-lookup"><span data-stu-id="b253d-396">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b253d-397">(Для качественных тестов задается тип испытания <strong>Параметры</strong> на странице <strong>Тесты</strong>.) Используйте страницу <strong>Группы проверки</strong>, чтобы назначить тестовую переменную и результат по умолчанию для отдельного качественного испытания.</span><span class="sxs-lookup"><span data-stu-id="b253d-397">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="b253d-398">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="b253d-398">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b253d-399">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="b253d-399">This inspection test has of several variables.</span></span> <span data-ttu-id="b253d-400">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="b253d-400">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b253d-401">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="b253d-401">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="b253d-402">Для каждого результата назначен статус <strong>положительного</strong> или <strong>отрицательного</strong> результата.</span><span class="sxs-lookup"><span data-stu-id="b253d-402">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="b253d-403">В ходе проверки каждой переменной инспектор создает отчет о результатах, выбирая один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="b253d-403">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="b253d-404">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b253d-404">Additional resources</span></span>
--------

[<span data-ttu-id="b253d-405">Процессы управления качеством</span><span class="sxs-lookup"><span data-stu-id="b253d-405">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="b253d-406">Управление несоответствием</span><span class="sxs-lookup"><span data-stu-id="b253d-406">Nonconformance management</span></span>](enable-nonconformance-management.md)
