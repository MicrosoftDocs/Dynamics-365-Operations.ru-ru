---
title: Сопоставления контроля качества
description: В этом разделе описывается, как можно использовать сопоставления контроля качества в Microsoft Dynamics 365 Supply Chain Management для автоматического создания заказов контроля качества, связанных с процессами продаж, покупки и производства.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956801"
---
# <a name="quality-associations"></a><span data-ttu-id="df43c-103">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="df43c-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df43c-104">В этом разделе описывается, как можно использовать сопоставления контроля качества в Microsoft Dynamics 365 Supply Chain Management для автоматического создания заказов контроля качества, связанных с процессами продаж, покупки и производства.</span><span class="sxs-lookup"><span data-stu-id="df43c-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="df43c-105">Ассоциация качества определяет всю следующую информацию для созданного заказа для контроля качества:</span><span class="sxs-lookup"><span data-stu-id="df43c-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="df43c-106">Событие проводки</span><span class="sxs-lookup"><span data-stu-id="df43c-106">The transaction event</span></span>
- <span data-ttu-id="df43c-107">Набор проверок, которые необходимо выполнить для номенклатур</span><span class="sxs-lookup"><span data-stu-id="df43c-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="df43c-108">Допустимый уровень качества (AQL)</span><span class="sxs-lookup"><span data-stu-id="df43c-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="df43c-109">План выборочного контроля</span><span class="sxs-lookup"><span data-stu-id="df43c-109">The sampling plan</span></span>

<span data-ttu-id="df43c-110">Необходимо определить сопоставление контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказов для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="df43c-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="df43c-111">Например, заказ для контроля качества может создаваться в бизнес-процессах для заказов на покупку, карантинных заказов, заказов на продажу и производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="df43c-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="df43c-112">Работа с сопоставлениями контроля качества</span><span class="sxs-lookup"><span data-stu-id="df43c-112">Working with quality associations</span></span>

<span data-ttu-id="df43c-113">Бизнес-процесс, использующий сопоставления, может быть связан с различными исходными документами, такими как заказы на покупку, заказы на продажу и производственные заказы.</span><span class="sxs-lookup"><span data-stu-id="df43c-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="df43c-114">Каждая запись сопоставления качества определяет также набор тестов, AQL и план выборочного контроля, применимые для создаваемых автоматически качественных заказов.</span><span class="sxs-lookup"><span data-stu-id="df43c-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="df43c-115">Необходимо определить запись сопоставления контроля качества для каждого изменения бизнес-процесса, требующего автоматического создания заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="df43c-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="df43c-116">Например, можно создать сопоставление, которое формирует заказ контроля качества для заказов на продажу, когда обновляется поступление продуктов по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="df43c-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="df43c-117">В зависимости от настройки плана выполнения сам процесс запуска может быть заблокирован при наличии открытого заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="df43c-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="df43c-118">Кроме того, могут быть заблокированы последующие процессы, такие как выставление накладных по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="df43c-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="df43c-119">Пока имеются открытые заказы для контроля качества, количества запасов автоматически блокируются по выдаче.</span><span class="sxs-lookup"><span data-stu-id="df43c-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="df43c-120">В зависимости от настройки поля **Полная блокировка** на странице **Выборка номенклатур**, количество равно количеству в заказе для контроля качества или количеству в строке исходного документа.</span><span class="sxs-lookup"><span data-stu-id="df43c-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="df43c-121">Дополнительные сведения см. в разделе [Выборка номенклатур управления качеством](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="df43c-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="df43c-122">Сопоставление по контролю качестве указывает событие и условия, при которых формируется заказ на контроль качества для определенного бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="df43c-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="df43c-123">Условия могут быть заданы для определенного места или юридического лица.</span><span class="sxs-lookup"><span data-stu-id="df43c-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="df43c-124">Заказ по контролю качества, в котором используются разрушающие испытания, может формироваться, только если для данного события имеется складской запас.</span><span class="sxs-lookup"><span data-stu-id="df43c-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="df43c-125">Для работы с сопоставлениями контроля качества выберите **Управление запасами \> Настройка \> Контроль качества \> Сопоставления контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="df43c-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="df43c-126">Следующие примеры показывают определение записи сопоставления качества для отклонений в бизнес-процессах.</span><span class="sxs-lookup"><span data-stu-id="df43c-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="df43c-127">Примеры обобщаются также в следующей таблице в плане событий и условий, определенных записью сопоставления качества.</span><span class="sxs-lookup"><span data-stu-id="df43c-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df43c-128">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="df43c-128">Reference type</span></span></th>
<th><span data-ttu-id="df43c-129">Тип события</span><span class="sxs-lookup"><span data-stu-id="df43c-129">Event type</span></span></th>
<th><span data-ttu-id="df43c-130">Выполнение</span><span class="sxs-lookup"><span data-stu-id="df43c-130">Execution</span></span></th>
<th><span data-ttu-id="df43c-131">Блокировка событий</span><span class="sxs-lookup"><span data-stu-id="df43c-131">Event blocking</span></span></th>
<th><span data-ttu-id="df43c-132">Ссылка на документ</span><span class="sxs-lookup"><span data-stu-id="df43c-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df43c-133">Запасы</span><span class="sxs-lookup"><span data-stu-id="df43c-133">Inventory</span></span></td>
<td><span data-ttu-id="df43c-134">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="df43c-134">Not applicable</span></span></td>
<td><span data-ttu-id="df43c-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="df43c-135">Not applicable</span></span></td>
<td><span data-ttu-id="df43c-136">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-136">None</span></span></td>
<td><span data-ttu-id="df43c-137">Все</span><span class="sxs-lookup"><span data-stu-id="df43c-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="df43c-138">Прод.</span><span class="sxs-lookup"><span data-stu-id="df43c-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="df43c-139">Процесс комплектации запланирован</span><span class="sxs-lookup"><span data-stu-id="df43c-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="df43c-140">До</span><span class="sxs-lookup"><span data-stu-id="df43c-140">Before</span></span></td>
<td><span data-ttu-id="df43c-141">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="df43c-142">Только определенный код, группа или все</span><span class="sxs-lookup"><span data-stu-id="df43c-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-143">Процесс комплектации</span><span class="sxs-lookup"><span data-stu-id="df43c-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-144">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="df43c-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-145">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="df43c-146">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="df43c-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-147">До</span><span class="sxs-lookup"><span data-stu-id="df43c-147">Before</span></span></td>
<td><span data-ttu-id="df43c-148">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-149">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="df43c-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-150">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="df43c-151">Покупка</span><span class="sxs-lookup"><span data-stu-id="df43c-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="df43c-152">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="df43c-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="df43c-153">До</span><span class="sxs-lookup"><span data-stu-id="df43c-153">Before</span></span></td>
<td><span data-ttu-id="df43c-154">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-155">Список поступлений</span><span class="sxs-lookup"><span data-stu-id="df43c-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-156">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-157">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="df43c-158">После</span><span class="sxs-lookup"><span data-stu-id="df43c-158">After</span></span></td>
<td><span data-ttu-id="df43c-159">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-160">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-161">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="df43c-162">Регистрация</span><span class="sxs-lookup"><span data-stu-id="df43c-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-163">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="df43c-163">Not applicable</span></span></td>
<td><span data-ttu-id="df43c-164">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-165">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-166">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="df43c-167">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-168">До</span><span class="sxs-lookup"><span data-stu-id="df43c-168">Before</span></span></td>
<td><span data-ttu-id="df43c-169">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-170">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-171">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="df43c-172">После</span><span class="sxs-lookup"><span data-stu-id="df43c-172">After</span></span></td>
<td><span data-ttu-id="df43c-173">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-174">Счет</span><span class="sxs-lookup"><span data-stu-id="df43c-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="df43c-175">Производство</span><span class="sxs-lookup"><span data-stu-id="df43c-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-176">Регистрация</span><span class="sxs-lookup"><span data-stu-id="df43c-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-177">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="df43c-177">Not applicable</span></span></td>
<td><span data-ttu-id="df43c-178">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="df43c-179">Все</span><span class="sxs-lookup"><span data-stu-id="df43c-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-180">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-181">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="df43c-182">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-183">До</span><span class="sxs-lookup"><span data-stu-id="df43c-183">Before</span></span></td>
<td><span data-ttu-id="df43c-184">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-185">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-186">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="df43c-187">После</span><span class="sxs-lookup"><span data-stu-id="df43c-187">After</span></span></td>
<td><span data-ttu-id="df43c-188">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-189">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="df43c-190">Карантин</span><span class="sxs-lookup"><span data-stu-id="df43c-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-191">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="df43c-192">До</span><span class="sxs-lookup"><span data-stu-id="df43c-192">Before</span></span></td>
<td><span data-ttu-id="df43c-193">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-194">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-195">После</span><span class="sxs-lookup"><span data-stu-id="df43c-195">After</span></span></td>
<td><span data-ttu-id="df43c-196">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-197">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-197">End</span></span></td>
<td><span data-ttu-id="df43c-198">До</span><span class="sxs-lookup"><span data-stu-id="df43c-198">Before</span></span></td>
<td><span data-ttu-id="df43c-199">Конец</span><span class="sxs-lookup"><span data-stu-id="df43c-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="df43c-200">Операция маршрута</span><span class="sxs-lookup"><span data-stu-id="df43c-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-201">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="df43c-202">До</span><span class="sxs-lookup"><span data-stu-id="df43c-202">Before</span></span></td>
<td><span data-ttu-id="df43c-203">Не допускается</span><span class="sxs-lookup"><span data-stu-id="df43c-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-204">Определенный код, группа или все конкретный ресурс, группа или все</span><span class="sxs-lookup"><span data-stu-id="df43c-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-205">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-206">После</span><span class="sxs-lookup"><span data-stu-id="df43c-206">After</span></span></td>
<td><span data-ttu-id="df43c-207">Не допускается</span><span class="sxs-lookup"><span data-stu-id="df43c-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="df43c-208">Производство сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="df43c-208">Co-product production</span></span></td>
<td><span data-ttu-id="df43c-209">Регистрация</span><span class="sxs-lookup"><span data-stu-id="df43c-209">Registration</span></span></td>
<td><span data-ttu-id="df43c-210">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="df43c-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-211">Не допускается</span><span class="sxs-lookup"><span data-stu-id="df43c-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="df43c-212">Все</span><span class="sxs-lookup"><span data-stu-id="df43c-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="df43c-213">Приемка</span><span class="sxs-lookup"><span data-stu-id="df43c-213">Report as finished</span></span></td>
<td><span data-ttu-id="df43c-214">До</span><span class="sxs-lookup"><span data-stu-id="df43c-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-215">После</span><span class="sxs-lookup"><span data-stu-id="df43c-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="df43c-216">Функция *Управление качеством для складских процессов* добавляет возможности для обработки заказов для контроля качества для производства, когда для поля **Тип события** задано значение *Приемка*, а для поля **Выполнение** задано значение *После*, и для покупок, для которых **Тип события** имеет значение *Регистрация*.</span><span class="sxs-lookup"><span data-stu-id="df43c-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="df43c-217">Подробнее см. в разделе [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="df43c-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="df43c-218">В таблице ниже приведены дополнительные сведения о том, как формируются заказы для определенных типов процессов.</span><span class="sxs-lookup"><span data-stu-id="df43c-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="df43c-219">Тип процесса</span><span class="sxs-lookup"><span data-stu-id="df43c-219">Type of process</span></span></th>
<th><span data-ttu-id="df43c-220">Когда можно автоматически формировать заказы по контролю качества</span><span class="sxs-lookup"><span data-stu-id="df43c-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="df43c-221">Когда можно формировать заказа, если применяются разрушающие испытания</span><span class="sxs-lookup"><span data-stu-id="df43c-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="df43c-222">Описание условия</span><span class="sxs-lookup"><span data-stu-id="df43c-222">Condition information</span></span></th>
<th><span data-ttu-id="df43c-223">Сведения о ручном формировании</span><span class="sxs-lookup"><span data-stu-id="df43c-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df43c-224">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="df43c-224">Purchase order</span></span></td>
<td><span data-ttu-id="df43c-225">До или после разноски поступления продуктов получаемого материала</span><span class="sxs-lookup"><span data-stu-id="df43c-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="df43c-226">После разноски отборочной накладной на полученные материалы, поскольку материалы должны быть доступны для проведения испытаний с разрушением.</span><span class="sxs-lookup"><span data-stu-id="df43c-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="df43c-227">Потребность в заказе на контроль может отражать конкретный сайт, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="df43c-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="df43c-228">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="df43c-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-229">Карантинный заказ</span><span class="sxs-lookup"><span data-stu-id="df43c-229">Quarantine order</span></span></td>
<td><span data-ttu-id="df43c-230">До или после завершения карантинного заказа</span><span class="sxs-lookup"><span data-stu-id="df43c-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="df43c-231">Нельзя формировать заказы с разрушительными испытаниями.</span><span class="sxs-lookup"><span data-stu-id="df43c-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="df43c-232">Предполагается, что функции карантинного заказа учитывают разрушаемые материалы.</span><span class="sxs-lookup"><span data-stu-id="df43c-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="df43c-233">Потребность в заказе на контроль может отражать конкретный сайт, номенклатуру или поставщика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="df43c-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="df43c-234">Созданный вручную качественный заказ, относящийся к карантинному заказу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="df43c-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-235">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="df43c-235">Sales order</span></span></td>
<td><span data-ttu-id="df43c-236">Перед обновлением запланированного процесса комплектации или отборочной накладной для отгружаемых номенклатур</span><span class="sxs-lookup"><span data-stu-id="df43c-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="df43c-237">В любом шаге</span><span class="sxs-lookup"><span data-stu-id="df43c-237">At any step</span></span></td>
<td><span data-ttu-id="df43c-238">Потребность в заказе на контроль может отражать конкретный объект, номенклатуру или заказчика, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="df43c-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="df43c-239">Созданный вручную качественный заказ, относящийся к заказу на продажу, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="df43c-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-240">Производственный заказ</span><span class="sxs-lookup"><span data-stu-id="df43c-240">Production order</span></span></td>
<td><span data-ttu-id="df43c-241">До или после регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="df43c-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="df43c-242">После регистрации завершенного количества для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="df43c-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="df43c-243">Потребность в заказе на контроль может отражать конкретный сайт, номенклатуру или сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="df43c-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="df43c-244">Созданный вручную качественный заказ, относящийся к производственному заказу может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="df43c-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-245">Производственный заказ с операцией маршрута</span><span class="sxs-lookup"><span data-stu-id="df43c-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="df43c-246">До или после завершения отчета по операции</span><span class="sxs-lookup"><span data-stu-id="df43c-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="df43c-247">После регистрации завершения производства по последней операции</span><span class="sxs-lookup"><span data-stu-id="df43c-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="df43c-248">Потребность в заказе на контроль может отражать конкретный объект, ресурс операции, либо сочетание этих условий.</span><span class="sxs-lookup"><span data-stu-id="df43c-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="df43c-249">Созданный вручную заказ для контроля качества, относящийся к операции маршрута, может использовать информацию из записи сопоставления качества, например план выборочного контроля, для расчета тестируемого количества, которое зависит от объема заказа.</span><span class="sxs-lookup"><span data-stu-id="df43c-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df43c-250">Запасы</span><span class="sxs-lookup"><span data-stu-id="df43c-250">Inventory</span></span></td>
<td><span data-ttu-id="df43c-251">Заказ для контроля качества не может быть создан автоматически для проводки в журнале запасов (например, журнал прибылей и убытков или журнал инвентаризации) или для проводок заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="df43c-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="df43c-252">Невозможно создать заказ контроля качества для складского количества номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="df43c-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="df43c-253">Требуются физические запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="df43c-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="df43c-254">Примеры автоматического создания заказов для контроля качества</span><span class="sxs-lookup"><span data-stu-id="df43c-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="df43c-255">Закупки</span><span class="sxs-lookup"><span data-stu-id="df43c-255">Purchasing</span></span>

<span data-ttu-id="df43c-256">В случае покупки, если для поля **тип события** выбрано *Поступление продуктов* а для поля **Выполнение** выбрано *После* на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="df43c-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="df43c-257">Если для параметра **На обновленное количество** указано значение *Да*, заказ контроля качества создается для каждого поступления по заказу на покупку на основе полученного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="df43c-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="df43c-258">При каждом получении количества по заказу на покупку создаются новые заказы контроля качества на основе вновь полученного количества.</span><span class="sxs-lookup"><span data-stu-id="df43c-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="df43c-259">Если для параметра **На обновленное количество** указано значение *Нет*, заказ для контроля качества создается для первого поступления по заказу на покупку на основе полученного количества.</span><span class="sxs-lookup"><span data-stu-id="df43c-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="df43c-260">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания.</span><span class="sxs-lookup"><span data-stu-id="df43c-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="df43c-261">Заказы для контроля качества не создаются для последующих поступлений по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="df43c-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="df43c-262">Рабочий</span><span class="sxs-lookup"><span data-stu-id="df43c-262">Production</span></span>

<span data-ttu-id="df43c-263">В случае производства, если для поля **тип события** выбрано *Приемка* а для поля **Выполнение** выбрано *После* на странице **Сопоставления контроля качества** , будут получены следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="df43c-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="df43c-264">Если для параметра **На обновленное количество** указано значение *Да*, заказ для контроля качества создается на основе каждого законченного количества и параметров для выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="df43c-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="df43c-265">При каждом принятом количестве в отношении производственный заказа создаются новые заказы для контроля качества на основе нового законченного количества.</span><span class="sxs-lookup"><span data-stu-id="df43c-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="df43c-266">Эта логика создания согласуется с покупкой.</span><span class="sxs-lookup"><span data-stu-id="df43c-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="df43c-267">Если для параметра **На обновленное количество** указано значение *Нет*, заказ для контроля качества создается при первом сообщении о том, что количество принято, на основе законченного количества.</span><span class="sxs-lookup"><span data-stu-id="df43c-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="df43c-268">Кроме того, один или несколько заказов для контроля качества создаются на основе оставшегося количества, в зависимости от аналитик отслеживания выборки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="df43c-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="df43c-269">Заказы для контроля качества не создаются для последующих законченных количеств.</span><span class="sxs-lookup"><span data-stu-id="df43c-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df43c-270">Спецификация качества</span><span class="sxs-lookup"><span data-stu-id="df43c-270">Quality specification</span></span></th>
<th><span data-ttu-id="df43c-271">На обновленное количество</span><span class="sxs-lookup"><span data-stu-id="df43c-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="df43c-272">На аналитику отслеживания</span><span class="sxs-lookup"><span data-stu-id="df43c-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="df43c-273">Результат</span><span class="sxs-lookup"><span data-stu-id="df43c-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df43c-274">Процент: 10%</span><span class="sxs-lookup"><span data-stu-id="df43c-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="df43c-275">Да</span><span class="sxs-lookup"><span data-stu-id="df43c-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="df43c-276">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-276">Batch number: No</span></span></p>
<p><span data-ttu-id="df43c-277">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="df43c-278">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="df43c-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="df43c-279">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="df43c-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="df43c-280">Заказ для контроля качества 1 для 3 (10% от 30)</span><span class="sxs-lookup"><span data-stu-id="df43c-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="df43c-281">Приемка для 70</span><span class="sxs-lookup"><span data-stu-id="df43c-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="df43c-282">Заказ для контроля качества 2 для 7 (10% от оставшегося количества заказа, что соответствует 70 в этом случае)</span><span class="sxs-lookup"><span data-stu-id="df43c-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="df43c-283">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="df43c-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="df43c-284">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-284">No</span></span></td>
<td>
<p><span data-ttu-id="df43c-285">Номер партии: Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-285">Batch number: No</span></span></p>
<p><span data-ttu-id="df43c-286">Серийный номер: Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="df43c-287">Количество в заказе: 100</span><span class="sxs-lookup"><span data-stu-id="df43c-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="df43c-288">Приемка для 30</span><span class="sxs-lookup"><span data-stu-id="df43c-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="df43c-289">Заказ для контроля качества 1 для 1 (для первого принятого количества, которое имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="df43c-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="df43c-290">Заказ для контроля качества 2 для 1 (для оставшегося количества, которое все еще имеет фиксированное значение 1)</span><span class="sxs-lookup"><span data-stu-id="df43c-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="df43c-291">Приемка для 10</span><span class="sxs-lookup"><span data-stu-id="df43c-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="df43c-292">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="df43c-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="df43c-293">Приемка для 60</span><span class="sxs-lookup"><span data-stu-id="df43c-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="df43c-294">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="df43c-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="df43c-295">Фиксированное количество: 1</span><span class="sxs-lookup"><span data-stu-id="df43c-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="df43c-296">Да</span><span class="sxs-lookup"><span data-stu-id="df43c-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="df43c-297">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="df43c-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="df43c-298">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="df43c-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="df43c-299">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="df43c-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="df43c-300">Приемка для 3: 1 для номера партии b1, серийный номер s1; 1 для номера партии b2, серийный номер s2; и 1 для номера партии b3, серийный номер s3</span><span class="sxs-lookup"><span data-stu-id="df43c-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="df43c-301">Заказ для контроля качества 1 для 1 партии номер b1, серийный номер s1</span><span class="sxs-lookup"><span data-stu-id="df43c-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="df43c-302">Заказ для контроля качества 2 для 1 партии номер b2, серийный номер s2</span><span class="sxs-lookup"><span data-stu-id="df43c-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="df43c-303">Заказ для контроля качества 3 для 1 партии номер b3, серийный номер s3</span><span class="sxs-lookup"><span data-stu-id="df43c-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="df43c-304">Приемка для 2: 1 для номера партии b4, серийного номера s4; и 1 для номера партии b5, серийный номер s5</span><span class="sxs-lookup"><span data-stu-id="df43c-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="df43c-305">Заказ для контроля качества 4 для 1 партии номер b4, серийный номер s4</span><span class="sxs-lookup"><span data-stu-id="df43c-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="df43c-306">Заказ для контроля качества 5 для 1 партии номер b5, серийный номер s5</span><span class="sxs-lookup"><span data-stu-id="df43c-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="df43c-307"><strong>Примечание:</strong> партия может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="df43c-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="df43c-308">Фиксированное количество: 2</span><span class="sxs-lookup"><span data-stu-id="df43c-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="df43c-309">Нет</span><span class="sxs-lookup"><span data-stu-id="df43c-309">No</span></span></td>
<td>
<p><span data-ttu-id="df43c-310">Номер партии: Да</span><span class="sxs-lookup"><span data-stu-id="df43c-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="df43c-311">Серийный номер: Да</span><span class="sxs-lookup"><span data-stu-id="df43c-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="df43c-312">Количество в заказе: 10</span><span class="sxs-lookup"><span data-stu-id="df43c-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="df43c-313">Приемка для 4: 1 для номера партии b1, серийный номер s1; 1 для номера партии b2, серийный номер s2; и 1 для номера партии b3, серийный номер s3; и 1 для номера партии b4, серийный номер s4</span><span class="sxs-lookup"><span data-stu-id="df43c-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="df43c-314">Заказ для контроля качества 1 для 1 партии номер b1, серийный номер s1</span><span class="sxs-lookup"><span data-stu-id="df43c-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="df43c-315">Заказ для контроля качества 2 для 1 партии номер b2, серийный номер s2</span><span class="sxs-lookup"><span data-stu-id="df43c-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="df43c-316">Заказ для контроля качества 3 для 1 партии номер b3, серийный номер s3</span><span class="sxs-lookup"><span data-stu-id="df43c-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="df43c-317">Заказ для контроля качества 4 для 1 партии номер b4, серийный номер s4</span><span class="sxs-lookup"><span data-stu-id="df43c-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="df43c-318">Заказ для контроля качества 5 для 2, без ссылки на номер партии и серийный номер</span><span class="sxs-lookup"><span data-stu-id="df43c-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="df43c-319">Приемка для 6: 1 для номера партии b5, серийный номер s5; 1 для номера партии b6, серийный номер s6; 1 для номера партии b7, серийного номера s7; 1 для номера партии b8, серийный номер s8; 1 для номера партии b9, серийного номера s9; и 1 для номера партии b10, серийный номер s10</span><span class="sxs-lookup"><span data-stu-id="df43c-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="df43c-320">Заказы для контроля качества не создаются.</span><span class="sxs-lookup"><span data-stu-id="df43c-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="df43c-321">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df43c-321">Additional resources</span></span>

- [<span data-ttu-id="df43c-322">Процессы управления качеством</span><span class="sxs-lookup"><span data-stu-id="df43c-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="df43c-323">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="df43c-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="df43c-324">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="df43c-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
