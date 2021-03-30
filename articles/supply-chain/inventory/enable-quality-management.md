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
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65858838b0fbb245a9330fab4e3b65b36a9eb944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219373"
---
# <a name="quality-management-overview"></a><span data-ttu-id="5b441-103">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="5b441-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b441-104">Эта тема описывает, как можно использовать управление качеством в Dynamics 365 Supply Chain Management, чтобы улучшить качество продукта в вашей цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="5b441-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="5b441-105">Управление качеством может помочь вам управлять периодами оборота, когда вы работаете с несоответствующими продуктами, независимо от их источника происхождения.</span><span class="sxs-lookup"><span data-stu-id="5b441-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="5b441-106">Поскольку диагностические типы связаны с отчетностью о коррекции, Supply Chain Management может планировать задачи для исправления проблем и предотвращения их повторения.</span><span class="sxs-lookup"><span data-stu-id="5b441-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="5b441-107">В дополнение к функциональности для управляя несоответствием, управление качеством включает функциональность для отслеживания проблем по типу проблемы (даже внутренние проблемы), и для определения решений как краткосрочные или долгосрочные.</span><span class="sxs-lookup"><span data-stu-id="5b441-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="5b441-108">Статистика по ключевым индикаторам производительности обеспечивает анализ истории предыдущих проблем несоответствия и решений, которые были применены для их исправления.</span><span class="sxs-lookup"><span data-stu-id="5b441-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="5b441-109">Вы можете использовать исторические данные для просмотра эффективности предыдущих мер по обеспечению качества и определить соответствующие меры для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="5b441-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="5b441-110">При указании сопоставления контроля качества Supply Chain Management может сформировать заказы по контролю качества для различных бизнес-процессов, событий и условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="5b441-111">Сопоставление может относиться к определенной номенклатуре, группе или ко всем продуктам.</span><span class="sxs-lookup"><span data-stu-id="5b441-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="5b441-112">Примеры использования управления качеством</span><span class="sxs-lookup"><span data-stu-id="5b441-112">Examples of the use of quality management</span></span>
<span data-ttu-id="5b441-113">Управление качеством гибкое и может быть реализована различными способами для соответствия требованиям определенных уровней операций цепочки снабжения.</span><span class="sxs-lookup"><span data-stu-id="5b441-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="5b441-114">Следующие примеры иллюстрируют возможное использование этих функций.</span><span class="sxs-lookup"><span data-stu-id="5b441-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="5b441-115">Автоматический запуск процесса контроля качества, основанный на предопределенных критериях (после регистрации на складе заказа на покупку от определенного поставщика).</span><span class="sxs-lookup"><span data-stu-id="5b441-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="5b441-116">Блокировка запасов во время проверки для исключения использования неутвержденных запасов (полная блокировка количеств по заказу на покупку).</span><span class="sxs-lookup"><span data-stu-id="5b441-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="5b441-117">Использование выборочного контроля номенклатур в рамках ассоциации качества для того, чтобы определить сумму текущих физических запасов, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="5b441-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="5b441-118">Выборочный контроль может быть основан на фиксированных количествах, на процентном объеме или на полном грузоместе.</span><span class="sxs-lookup"><span data-stu-id="5b441-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="5b441-119">Функция _Управление качеством для складских процессов_ расширяет возможности управления качеством.</span><span class="sxs-lookup"><span data-stu-id="5b441-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="5b441-120">При использовании этой функции см. раздел [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md), чтобы просмотреть примеры работы модуля управления качеством, когда он включен.</span><span class="sxs-lookup"><span data-stu-id="5b441-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="5b441-121">Создайте заказы для контроля качества для частичных приемок.</span><span class="sxs-lookup"><span data-stu-id="5b441-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="5b441-122">Чтобы создать заказ для контроля качества, основанный на количестве, физически полученном с заказом, необходимо установить флажок **На обновленное количество** в форме **Выборка элементов**.</span><span class="sxs-lookup"><span data-stu-id="5b441-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="5b441-123">Создание типов испытаний, которые включают минимальные, максимальные и целевые значения испытаний, и выполнение качественного или количественного тестирования с предопределенными результатами проверки.</span><span class="sxs-lookup"><span data-stu-id="5b441-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="5b441-124">Указание допустимого уровня качества (AQL) для управления допусками измерения качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="5b441-125">Указание ресурсов, которые требуются для контрольной операции, например испытательный участок и инструменты для испытаний.</span><span class="sxs-lookup"><span data-stu-id="5b441-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="5b441-126">Работа с сопоставлениями контроля качества</span><span class="sxs-lookup"><span data-stu-id="5b441-126">Working with quality associations</span></span>
<span data-ttu-id="5b441-127">Бизнес-процесс, использующий сопоставления, может быть связан с различными исходными документами, такими как заказы на покупку, заказы на продажу и производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="5b441-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="5b441-128">Каждая запись сопоставления качества определяет также набор тестов, AQL и план выборочного контроля, применимые для создаваемых автоматически качественных заказов.</span><span class="sxs-lookup"><span data-stu-id="5b441-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="5b441-129">Необходимо определить запись сопоставления контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="5b441-130">Например, можно создать сопоставление, которое формирует заказ контроля качества для заказов на продажу, когда обновляется поступление продуктов по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="5b441-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="5b441-131">В зависимости от настройки плана исполнения возможна блокировка самого запускающего процесса, пока имеется открытый заказ для контроля качества, или блокировка следующих процессов, таких как выставление накладной по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="5b441-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="5b441-132">**Примечание.** Пока имеются открытые заказы для контроля качества, количества запасов автоматически блокируются по выдаче.</span><span class="sxs-lookup"><span data-stu-id="5b441-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="5b441-133">В зависимости от настройки **Полная блокировка** на странице **Выборка номенклатур**, количество равно количеству в заказе для контроля качества или количеству в строке исходного документа.</span><span class="sxs-lookup"><span data-stu-id="5b441-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="5b441-134">Сопоставление по контролю качестве указывает событие и условия, при которых формируется заказ на контроль качества для определенного бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="5b441-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="5b441-135">Условия могут быть заданы для определенного места или юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5b441-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="5b441-136">Заказ по контролю качества, в котором используются разрушающие испытания, может формироваться, только если для данного события имеется складской запас.</span><span class="sxs-lookup"><span data-stu-id="5b441-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="5b441-137">Следующие примеры иллюстрируют определение записи сопоставления качества для отклонений в бизнес-процессах.</span><span class="sxs-lookup"><span data-stu-id="5b441-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="5b441-138">Примеры обобщаются также в следующей таблице в плане событий и условий, определенных записью сопоставления качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b441-139">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="5b441-139">Reference type</span></span></th>
<th><span data-ttu-id="5b441-140">Тип события</span><span class="sxs-lookup"><span data-stu-id="5b441-140">Event type</span></span></th>
<th><span data-ttu-id="5b441-141">Выполнение</span><span class="sxs-lookup"><span data-stu-id="5b441-141">Execution</span></span></th>
<th><span data-ttu-id="5b441-142">Блокировка событий</span><span class="sxs-lookup"><span data-stu-id="5b441-142">Event blocking</span></span></th>
<th><span data-ttu-id="5b441-143">Ссылка на документ</span><span class="sxs-lookup"><span data-stu-id="5b441-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b441-144">Запасы</span><span class="sxs-lookup"><span data-stu-id="5b441-144">Inventory</span></span></td>
<td><span data-ttu-id="5b441-145">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5b441-145">Not applicable</span></span></td>
<td><span data-ttu-id="5b441-146">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5b441-146">Not applicable</span></span></td>
<td><span data-ttu-id="5b441-147">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-147">None</span></span></td>
<td><span data-ttu-id="5b441-148">Все</span><span class="sxs-lookup"><span data-stu-id="5b441-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="5b441-149">Прод.</span><span class="sxs-lookup"><span data-stu-id="5b441-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="5b441-150">Процесс комплектации запланирован</span><span class="sxs-lookup"><span data-stu-id="5b441-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="5b441-151">До</span><span class="sxs-lookup"><span data-stu-id="5b441-151">Before</span></span></td>
<td><span data-ttu-id="5b441-152">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="5b441-153">Только определенный код, группа или все</span><span class="sxs-lookup"><span data-stu-id="5b441-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-154">Процесс комплектации</span><span class="sxs-lookup"><span data-stu-id="5b441-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-155">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="5b441-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-156">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b441-157">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="5b441-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-158">До</span><span class="sxs-lookup"><span data-stu-id="5b441-158">Before</span></span></td>
<td><span data-ttu-id="5b441-159">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-160">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="5b441-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-161">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="5b441-162">Покупка</span><span class="sxs-lookup"><span data-stu-id="5b441-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="5b441-163">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="5b441-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="5b441-164">До</span><span class="sxs-lookup"><span data-stu-id="5b441-164">Before</span></span></td>
<td><span data-ttu-id="5b441-165">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-166">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="5b441-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-167">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-168">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b441-169">После</span><span class="sxs-lookup"><span data-stu-id="5b441-169">After</span></span></td>
<td><span data-ttu-id="5b441-170">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-171">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-172">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b441-173">Регистрация</span><span class="sxs-lookup"><span data-stu-id="5b441-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-174">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5b441-174">Not applicable</span></span></td>
<td><span data-ttu-id="5b441-175">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-176">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-177">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b441-178">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-179">До</span><span class="sxs-lookup"><span data-stu-id="5b441-179">Before</span></span></td>
<td><span data-ttu-id="5b441-180">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-181">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-182">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b441-183">После</span><span class="sxs-lookup"><span data-stu-id="5b441-183">After</span></span></td>
<td><span data-ttu-id="5b441-184">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-185">Счет</span><span class="sxs-lookup"><span data-stu-id="5b441-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="5b441-186">Производство</span><span class="sxs-lookup"><span data-stu-id="5b441-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-187">Регистрация</span><span class="sxs-lookup"><span data-stu-id="5b441-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-188">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5b441-188">Not applicable</span></span></td>
<td><span data-ttu-id="5b441-189">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="5b441-190">Все</span><span class="sxs-lookup"><span data-stu-id="5b441-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-191">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-192">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b441-193">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-194">До</span><span class="sxs-lookup"><span data-stu-id="5b441-194">Before</span></span></td>
<td><span data-ttu-id="5b441-195">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-196">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-197">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b441-198">После</span><span class="sxs-lookup"><span data-stu-id="5b441-198">After</span></span></td>
<td><span data-ttu-id="5b441-199">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-200">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5b441-201">Карантин</span><span class="sxs-lookup"><span data-stu-id="5b441-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-202">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5b441-203">До</span><span class="sxs-lookup"><span data-stu-id="5b441-203">Before</span></span></td>
<td><span data-ttu-id="5b441-204">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-205">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-206">После</span><span class="sxs-lookup"><span data-stu-id="5b441-206">After</span></span></td>
<td><span data-ttu-id="5b441-207">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-208">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-208">End</span></span></td>
<td><span data-ttu-id="5b441-209">До</span><span class="sxs-lookup"><span data-stu-id="5b441-209">Before</span></span></td>
<td><span data-ttu-id="5b441-210">Конец</span><span class="sxs-lookup"><span data-stu-id="5b441-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b441-211">Операция маршрута</span><span class="sxs-lookup"><span data-stu-id="5b441-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-212">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5b441-213">До</span><span class="sxs-lookup"><span data-stu-id="5b441-213">Before</span></span></td>
<td><span data-ttu-id="5b441-214">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-215">Определенный код, группа или специфичный для ресурса, группа или все</span><span class="sxs-lookup"><span data-stu-id="5b441-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-216">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-217">После</span><span class="sxs-lookup"><span data-stu-id="5b441-217">After</span></span></td>
<td><span data-ttu-id="5b441-218">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b441-219">Производство сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="5b441-219">Co-product production</span></span></td>
<td><span data-ttu-id="5b441-220">Регистрация</span><span class="sxs-lookup"><span data-stu-id="5b441-220">Registration</span></span></td>
<td><span data-ttu-id="5b441-221">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5b441-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-222">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5b441-223">Все</span><span class="sxs-lookup"><span data-stu-id="5b441-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b441-224">Приемка</span><span class="sxs-lookup"><span data-stu-id="5b441-224">Report as finished</span></span></td>
<td><span data-ttu-id="5b441-225">До</span><span class="sxs-lookup"><span data-stu-id="5b441-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-226">После</span><span class="sxs-lookup"><span data-stu-id="5b441-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5b441-227">В таблице ниже приведены дополнительные сведения о том, как формируются заказы для определенных типов процессов.</span><span class="sxs-lookup"><span data-stu-id="5b441-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b441-228">Тип процесса</span><span class="sxs-lookup"><span data-stu-id="5b441-228">Type of process</span></span></th>
<th><span data-ttu-id="5b441-229">Когда можно автоматически формировать заказы по контролю качества</span><span class="sxs-lookup"><span data-stu-id="5b441-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="5b441-230">Когда можно формировать заказа, если применяются разрушающие испытания</span><span class="sxs-lookup"><span data-stu-id="5b441-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="5b441-231">Описание условия</span><span class="sxs-lookup"><span data-stu-id="5b441-231">Condition information</span></span></th>
<th><span data-ttu-id="5b441-232">Сведения о ручном формировании</span><span class="sxs-lookup"><span data-stu-id="5b441-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b441-233">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="5b441-233">Purchase order</span></span></td>
<td><span data-ttu-id="5b441-234">До или после разноски поступления продуктов получаемого материала</span><span class="sxs-lookup"><span data-stu-id="5b441-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="5b441-235">После разноски отборочной накладной на полученные материалы, поскольку материалы должны быть доступны для проведения испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="5b441-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="5b441-236">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b441-237">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="5b441-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-238">Карантинный заказ</span><span class="sxs-lookup"><span data-stu-id="5b441-238">Quarantine order</span></span></td>
<td><span data-ttu-id="5b441-239">До или после завершения карантинного заказа</span><span class="sxs-lookup"><span data-stu-id="5b441-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="5b441-240">Нельзя формировать заказы с разрушительными испытаниями.</span><span class="sxs-lookup"><span data-stu-id="5b441-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="5b441-241">Предполагается, что функции карантинного заказа учитывают разрушаемые материалы.</span><span class="sxs-lookup"><span data-stu-id="5b441-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="5b441-242">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b441-243">Созданный вручную качественный заказ, относящийся к карантинному заказу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="5b441-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-244">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="5b441-244">Sales order</span></span></td>
<td><span data-ttu-id="5b441-245">Перед обновлением запланированного процесса комплектации или отборочной накладной для отгружаемых номенклатур</span><span class="sxs-lookup"><span data-stu-id="5b441-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="5b441-246">В любом шаге</span><span class="sxs-lookup"><span data-stu-id="5b441-246">At any step</span></span></td>
<td><span data-ttu-id="5b441-247">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или заказчика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b441-248">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="5b441-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-249">Производственный заказ</span><span class="sxs-lookup"><span data-stu-id="5b441-249">Production order</span></span></td>
<td><span data-ttu-id="5b441-250">До или после регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="5b441-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5b441-251">После регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="5b441-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5b441-252">Потребность в заказе на контроль может отражать конкретный объект или номенклатуру, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b441-253">Созданный вручную качественный заказ, относящийся к производственному заказу может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="5b441-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-254">Производственный заказ с операцией маршрута</span><span class="sxs-lookup"><span data-stu-id="5b441-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="5b441-255">До или после завершения отчета по операции</span><span class="sxs-lookup"><span data-stu-id="5b441-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="5b441-256">После регистрации завершения производства по последней операции</span><span class="sxs-lookup"><span data-stu-id="5b441-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="5b441-257">Потребность в заказе на контроль может отражать конкретный объект, ресурс операции, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="5b441-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b441-258">Созданный вручную заказ для контроля качества, относящийся к операции маршрута, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="5b441-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b441-259">Запасы</span><span class="sxs-lookup"><span data-stu-id="5b441-259">Inventory</span></span></td>
<td><span data-ttu-id="5b441-260">Заказ для контроля качества не может быть создан автоматически для проводки в журнале запасов (например, журнал прибылей и убытков или журнал инвентаризации) или для проводок заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="5b441-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="5b441-261">Невозможно создать заказ контроля качества для складского количества номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5b441-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="5b441-262">Требуются физические запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="5b441-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="5b441-263">Примеры автоматического создания заказов для контроля качества</span><span class="sxs-lookup"><span data-stu-id="5b441-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="5b441-264">Закупки</span><span class="sxs-lookup"><span data-stu-id="5b441-264">Purchasing</span></span>

<span data-ttu-id="5b441-265">В случае покупки, если для поля **тип события** выбрано **Поступление продуктов** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="5b441-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="5b441-266">Если для параметра **На обновленное количество** указано значение **Да**, заказ контроля качества создается для каждого поступления по заказу на покупку на основе полученного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5b441-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="5b441-267">При каждом получении количества по заказу на покупку создаются новые заказы контроля качества на основе вновь полученного количества.</span><span class="sxs-lookup"><span data-stu-id="5b441-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="5b441-268">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается для первого поступления по заказу на покупку на основе полученного количества.</span><span class="sxs-lookup"><span data-stu-id="5b441-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="5b441-269">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания.</span><span class="sxs-lookup"><span data-stu-id="5b441-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="5b441-270">Заказы для контроля качества не создаются для последующих поступлений по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="5b441-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="5b441-271">Рабочий</span><span class="sxs-lookup"><span data-stu-id="5b441-271">Production</span></span>

<span data-ttu-id="5b441-272">В случае производства, если для поля **тип события** выбрано **Приемка** а для поля **Выполнение** выбрано **После** на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="5b441-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="5b441-273">Если для параметра **На обновленное количество** указано значение **Да**, заказ для контроля качества создается на основе каждого законченного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5b441-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="5b441-274">При каждом принятом количестве в отношении производственный заказа создаются новые заказы для контроля качества на основе нового законченного количества.</span><span class="sxs-lookup"><span data-stu-id="5b441-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="5b441-275">Эта логика создания согласуется с покупкой.</span><span class="sxs-lookup"><span data-stu-id="5b441-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="5b441-276">Если для параметра **На обновленное количество** указано значение **Нет**, заказ для контроля качества создается при первом сообщении о том, что количество принято, на основе законченного количества.</span><span class="sxs-lookup"><span data-stu-id="5b441-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="5b441-277">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5b441-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="5b441-278">Заказы для контроля качества не создаются для последующих законченных количеств.</span><span class="sxs-lookup"><span data-stu-id="5b441-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b441-279">Спецификация качества</span><span class="sxs-lookup"><span data-stu-id="5b441-279">Quality specification</span></span></th>
<th><span data-ttu-id="5b441-280">На обновленное количество</span><span class="sxs-lookup"><span data-stu-id="5b441-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="5b441-281">На аналитику отслеживания</span><span class="sxs-lookup"><span data-stu-id="5b441-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="5b441-282">Результат</span><span class="sxs-lookup"><span data-stu-id="5b441-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b441-283">Процент: 10%</span><span class="sxs-lookup"><span data-stu-id="5b441-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="5b441-284">Да</span><span class="sxs-lookup"><span data-stu-id="5b441-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b441-285">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-285">Batch number: No</span></span></p>
<p><span data-ttu-id="5b441-286">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b441-287">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="5b441-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="5b441-288">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="5b441-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b441-289">Заказ для контроля качества #1 для 3 (10% от 30)</span><span class="sxs-lookup"><span data-stu-id="5b441-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b441-290">Приемка для 70</span><span class="sxs-lookup"><span data-stu-id="5b441-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="5b441-291">Заказ для контроля качества #2 для 7 (10% от оставшегося количества заказа, что соответствует 70 в этом случае)</span><span class="sxs-lookup"><span data-stu-id="5b441-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b441-292">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="5b441-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b441-293">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-293">No</span></span></td>
<td>
<p><span data-ttu-id="5b441-294">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-294">Batch number: No</span></span></p>
<p><span data-ttu-id="5b441-295">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="5b441-296">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="5b441-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="5b441-297">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="5b441-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b441-298">Заказ для контроля качества #1 для 1 (для первого принятого количества, которое имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="5b441-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="5b441-299">Заказ для контроля качества #2 для 1 (для оставшегося количества, которое все еще имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="5b441-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b441-300">Приемка для 10</span><span class="sxs-lookup"><span data-stu-id="5b441-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="5b441-301">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="5b441-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b441-302">Приемка для 60</span><span class="sxs-lookup"><span data-stu-id="5b441-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="5b441-303">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="5b441-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b441-304">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="5b441-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b441-305">Да</span><span class="sxs-lookup"><span data-stu-id="5b441-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b441-306">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="5b441-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b441-307">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="5b441-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b441-308">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="5b441-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b441-309">Приемка для 3: 1 для #b1, #s1; 1 для #b2, #s2; и 1 для #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="5b441-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="5b441-310">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="5b441-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5b441-311">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="5b441-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5b441-312">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="5b441-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b441-313">Приемка для 2: 1 для #b4, #s4; и 1 для #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="5b441-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="5b441-314">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="5b441-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="5b441-315">Заказ для контроля качества #5 для 1 партии #b5, последовательный #s5</span><span class="sxs-lookup"><span data-stu-id="5b441-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="5b441-316"><strong>Примечание:</strong> партия может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="5b441-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b441-317">Фиксированное количество: 2</span><span class="sxs-lookup"><span data-stu-id="5b441-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="5b441-318">Нет</span><span class="sxs-lookup"><span data-stu-id="5b441-318">No</span></span></td>
<td>
<p><span data-ttu-id="5b441-319">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="5b441-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b441-320">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="5b441-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b441-321">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="5b441-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b441-322">Приемка для 4: 1 для #b1, #s1; 1 для #b2, #s2; 1 для #b3, #s3 и 1 для #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="5b441-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="5b441-323">Заказ для контроля качества #1 для 1 партии #b1, последовательный #s1</span><span class="sxs-lookup"><span data-stu-id="5b441-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5b441-324">Заказ для контроля качества #2 для 1 партии #b2, последовательный #s2</span><span class="sxs-lookup"><span data-stu-id="5b441-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5b441-325">Заказ для контроля качества #3 для 1 партии #b3, последовательный #s3</span><span class="sxs-lookup"><span data-stu-id="5b441-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="5b441-326">Заказ для контроля качества #4 для 1 партии #b4, последовательный #s4</span><span class="sxs-lookup"><span data-stu-id="5b441-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="5b441-327">Заказ для контроля качества #5 для 2, без ссылки на партию и серийный номер</span><span class="sxs-lookup"><span data-stu-id="5b441-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b441-328">Приемка для 6: 1 для #b5, #s5; 1 для #b6, #s6; 1 для #b7, #s7; 1 для #b8, #s8; 1 для #b9, #s9; и 1 для #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="5b441-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="5b441-329">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="5b441-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5b441-330">Функция *Управление качеством для складских процессов* добавляет возможности для обработки заказов для контроля качества для производства, когда для параметра **Тип события** задано значение *Приемка*, а для параметра **Выполнение** задано значение *После*, и для покупок, для которых **Тип события** имеет значение *Регистрация*.</span><span class="sxs-lookup"><span data-stu-id="5b441-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="5b441-331">Подробнее см. в разделе [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="5b441-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="5b441-332">Страницы управления качеством</span><span class="sxs-lookup"><span data-stu-id="5b441-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b441-333">Страница</span><span class="sxs-lookup"><span data-stu-id="5b441-333">Page</span></span></th>
<th><span data-ttu-id="5b441-334">описание</span><span class="sxs-lookup"><span data-stu-id="5b441-334">Description</span></span></th>
<th><span data-ttu-id="5b441-335">Пример</span><span class="sxs-lookup"><span data-stu-id="5b441-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b441-336">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="5b441-336">Quality associations</span></span></td>
<td><span data-ttu-id="5b441-337">См. предыдущие разделы этой статьи.</span><span class="sxs-lookup"><span data-stu-id="5b441-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="5b441-338">Ассоциация качества определяет всю следующую информацию для созданного заказа для контроля качества:</span><span class="sxs-lookup"><span data-stu-id="5b441-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="5b441-339">Событие проводки</span><span class="sxs-lookup"><span data-stu-id="5b441-339">The transaction event</span></span></li>
<li><span data-ttu-id="5b441-340">Набор проверок, которые необходимо выполнить для номенклатур</span><span class="sxs-lookup"><span data-stu-id="5b441-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="5b441-341">Допустимый уровень качества</span><span class="sxs-lookup"><span data-stu-id="5b441-341">The AQL</span></span></li>
<li><span data-ttu-id="5b441-342">План выборочного контроля</span><span class="sxs-lookup"><span data-stu-id="5b441-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="5b441-343">Необходимо определить сопоставление контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="5b441-344">Например, заказ для контроля качества может создаваться в бизнес-процессах для заказов на покупку, карантинных заказов, заказов на продажу и производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="5b441-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b441-345">Тесты</span><span class="sxs-lookup"><span data-stu-id="5b441-345">Tests</span></span></td>
<td><span data-ttu-id="5b441-346">Эта страница используется для назначения и просмотра отдельных испытаний, определяющих соответствие вашей продукции требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="5b441-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="5b441-347">Вы можете назначить одни или несколько индивидуальных испытаний в группе проверки.</span><span class="sxs-lookup"><span data-stu-id="5b441-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="5b441-348">В этом случае вы также определяете информацию, специфичную для теста, такую как приемлемые значения измерения.</span><span class="sxs-lookup"><span data-stu-id="5b441-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="5b441-349">Значения измерения используются для испытаний с количественными результатами, и переменные испытания используются для качественных испытаний.</span><span class="sxs-lookup"><span data-stu-id="5b441-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="5b441-350">Количественное испытание имеет тип испытания <strong>Целое число</strong> или <strong>Дробь</strong>, и также имеет обозначенную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="5b441-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="5b441-351">Спецификации качества и результаты теста выражаются числами.</span><span class="sxs-lookup"><span data-stu-id="5b441-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="5b441-352">Качественное испытание имеет тип проверки <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b441-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="5b441-353">Для качественных испытаний требуется дополнительная информация об измеряемой тестовой переменной и ее возможных перечислимых вариантах.</span><span class="sxs-lookup"><span data-stu-id="5b441-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="5b441-354">Спецификации качества и результаты теста выражаются в соответствии с результатом.</span><span class="sxs-lookup"><span data-stu-id="5b441-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="5b441-355">Производственная компания проводит два испытания купленных материалов: количественное испытание качества материала и качественную проверку повреждения упаковки.</span><span class="sxs-lookup"><span data-stu-id="5b441-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="5b441-356">Компания определяет дополнительную информацию о качественном испытании, чтобы идентифицировать переменную испытания (поврежденная упаковка) и ее результаты.</span><span class="sxs-lookup"><span data-stu-id="5b441-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="5b441-357">Компания использует страницу <strong>Группы проверки</strong> для того, чтобы назначить два испытания в группу проверки и указать информацию, специфичную для испытания.</span><span class="sxs-lookup"><span data-stu-id="5b441-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="5b441-358">Группа испытаний назначается заказу контроля качества, таким образом компания может составить отчет по результатам этих двух испытаний.</span><span class="sxs-lookup"><span data-stu-id="5b441-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b441-359">Группы проверки</span><span class="sxs-lookup"><span data-stu-id="5b441-359">Test groups</span></span></td>
<td><span data-ttu-id="5b441-360">Эта страница используется для настройки, изменения и просмотра групп проверки и отдельных проверок, включенных в проверочную группу.</span><span class="sxs-lookup"><span data-stu-id="5b441-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="5b441-361">В верхней области отображаются группы испытаний, а в нижней области отображаются испытания, включенные в выбранную группу испытаний.</span><span class="sxs-lookup"><span data-stu-id="5b441-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="5b441-362">Группе испытаний назначаются несколько политик, такие как план выборочного контроля, приемлемый уровень качества и потребности для испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="5b441-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="5b441-363">Когда вы назначаете индивидуальное испытание для контрольной группы, вы определяете дополнительную информацию, такую как последовательность, документы и даты срока действия.</span><span class="sxs-lookup"><span data-stu-id="5b441-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="5b441-364">Для количественного испытания информация, которую вы определяете, также включает приемлемые значения измерений.</span><span class="sxs-lookup"><span data-stu-id="5b441-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="5b441-365">Для качественного испытания информация включает переменную испытания и результат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b441-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="5b441-366">Группа проверок, назначенная заказу на контроль качества, определяет начальный набор испытаний, которые должны выполняться для указанной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5b441-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="5b441-367">Однако можно в заказе для контроля качества можно добавлять, удалять или изменять испытания.</span><span class="sxs-lookup"><span data-stu-id="5b441-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="5b441-368">Результаты проверок указываются для каждой проверки в заказе контроля качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="5b441-369">Производственная компания определяет группу испытаний для каждой разновидности своих инструкций по обеспечению качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="5b441-370">Разные группы испытаний отражают различия планов выборочного контроля, наборов испытаний, которые должны быть выполнены совместно, приемлемых уровней качества, а также других коэффициентов.</span><span class="sxs-lookup"><span data-stu-id="5b441-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="5b441-371">Для испытаний с количественными результатами также имеются различия в приемлемых значениях измерений.</span><span class="sxs-lookup"><span data-stu-id="5b441-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="5b441-372">Чтобы обеспечить принудительное выполнение инструкций по обеспечению качества, компания назначает проверочную группу для каждого правила автоматического создания заказов контроля качества (на странице <strong>Сопоставления контроля качества</strong>), а также назначает проверочную группу создаваемым вручную заказам для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b441-373">Группы контроля качества номенклатуры</span><span class="sxs-lookup"><span data-stu-id="5b441-373">Item quality groups</span></span></td>
<td><span data-ttu-id="5b441-374">Эта страница используется для настройки, изменения и просмотра номенклатур, назначенных группе контроля качества, или групп контроля качества, назначенных номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="5b441-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="5b441-375">Группа контроля качества определяет общие требования к проверке номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5b441-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="5b441-376">После определения требованиям к испытанию на странице <strong>Группы проверки</strong> вы можете определить правила для автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="5b441-377">Для того, чтобы упростить процесс, вы не определяете правила для индивидуальных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="5b441-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="5b441-378">Вместо этого вы определяете правила для группы качества путем использования страницы <strong>Сопоставления контроля качества</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b441-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="5b441-379">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной группы качества, чтобы назначить соответствующие номенклатуры для этой группы.</span><span class="sxs-lookup"><span data-stu-id="5b441-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="5b441-380">Вы можете также использовать страницу <strong>Группы контроля качества номенклатуры</strong> для выбранной номенклатуры, чтобы назначить соответствующую группу качества для этой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5b441-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="5b441-381">Производственная компания приобретает различные виды сырья, для которых действуют одинаковые требования по проверке во время входного контроля.</span><span class="sxs-lookup"><span data-stu-id="5b441-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="5b441-382">Компания определяет группу качества, и после этого назначает коды номенклатур, которые связаны с сырьем, для этой группы.</span><span class="sxs-lookup"><span data-stu-id="5b441-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="5b441-383">Позднее компания покупает новый тип сырья, которое имеет такие же требования к испытаниям.</span><span class="sxs-lookup"><span data-stu-id="5b441-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="5b441-384">Вместо настройки новых требований к испытаниям для нового материала компания добавляет код номенклатуры для нового материала к существующей группе качества.</span><span class="sxs-lookup"><span data-stu-id="5b441-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="5b441-385">Эта же производственная компания также производит номенклатуры, которые имеют одинаковые требования в отношении производственных испытаний и одинаковые требования в отношении проведения испытаний перед отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="5b441-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="5b441-386">Компания определяет две дополнительные группы контроля качества и назначает соответствующие коды номенклатур каждой группе.</span><span class="sxs-lookup"><span data-stu-id="5b441-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b441-387">Переменные проверки</span><span class="sxs-lookup"><span data-stu-id="5b441-387">Test variables</span></span></td>
<td><span data-ttu-id="5b441-388">Используйте эту страницу для определения и просмотра переменных, связанных с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="5b441-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="5b441-389">Для каждой переменной вы определяете перечислимые результаты, которые представляют возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="5b441-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="5b441-390">Вы определяете испытания на странице <strong>Тесты</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b441-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5b441-391">Для качественных тестов вы должны установить тип испытания <strong>Параметр</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b441-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="5b441-392">Используйте страницу <strong>Группы проверки</strong> для назначения тестовой переменной отдельному тесту.</span><span class="sxs-lookup"><span data-stu-id="5b441-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="5b441-393">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="5b441-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5b441-394">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="5b441-394">This inspection test has several variables.</span></span> <span data-ttu-id="5b441-395">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="5b441-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5b441-396">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="5b441-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b441-397">Результаты переменной проверки</span><span class="sxs-lookup"><span data-stu-id="5b441-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="5b441-398">Используйте эту страницу для настройки, изменения и просмотра возможных результатов испытаний тестовой переменной, связанной с качественным испытанием.</span><span class="sxs-lookup"><span data-stu-id="5b441-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="5b441-399">Для каждого результата назначается статус <strong>приемлемый</strong> или <strong>неприемлемый</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b441-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="5b441-400">Следует определить переменную и ее результаты для каждого качественного испытания, которое определено на странице <strong>Тесты</strong></span><span class="sxs-lookup"><span data-stu-id="5b441-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5b441-401">(Для качественных тестов задается тип испытания <strong>Параметры</strong> на странице <strong>Тесты</strong>.) Используйте страницу <strong>Группы проверки</strong>, чтобы назначить тестовую переменную и результат по умолчанию для отдельного качественного испытания.</span><span class="sxs-lookup"><span data-stu-id="5b441-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="5b441-402">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="5b441-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5b441-403">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="5b441-403">This inspection test has of several variables.</span></span> <span data-ttu-id="5b441-404">Одна из переменных — вкус, при этом возможные результаты для этой переменной — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="5b441-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5b441-405">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="5b441-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="5b441-406">Для каждого результата назначен статус <strong>положительного</strong> или <strong>отрицательного</strong> результата.</span><span class="sxs-lookup"><span data-stu-id="5b441-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="5b441-407">В ходе проверки каждой переменной инспектор создает отчет о результатах, выбирая один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="5b441-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="5b441-408">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b441-408">Additional resources</span></span>
--------

[<span data-ttu-id="5b441-409">Процессы управления качеством</span><span class="sxs-lookup"><span data-stu-id="5b441-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="5b441-410">Управление несоответствием</span><span class="sxs-lookup"><span data-stu-id="5b441-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="5b441-411">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="5b441-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]