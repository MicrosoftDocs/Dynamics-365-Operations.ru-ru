---
title: Цены продажи подписки
description: При создании подписки цена продажи извлекается из настройки цены продажи, созданной в форме "Цена продажи (подписка)".
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4b02af0a535e67818751c437482c3663524474
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817421"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="534b3-103">Цены продажи подписки</span><span class="sxs-lookup"><span data-stu-id="534b3-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="534b3-104">При создании подписки цена продажи извлекается из настройки цены продажи, созданной в форме **Цена продажи (подписка)**.</span><span class="sxs-lookup"><span data-stu-id="534b3-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="534b3-105">В форме **Цена продажи (подписка)** можно создать цену продажи для конкретной подписки или цены продажи, которые будут применяться более широко.</span><span class="sxs-lookup"><span data-stu-id="534b3-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="534b3-106">Чтобы цена продажи применялась для подписки, код периода и валюта подписки должны совпадать с кодом периода и валютой цены продажи.</span><span class="sxs-lookup"><span data-stu-id="534b3-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="534b3-107">Если код периода и валюта одинаковы для подписки и для цены продажи, цены продажи подписки выбираются на основе приоритетов, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="534b3-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="534b3-108">Отсутствие знака в ячейке соответствуют пустому полю, знак "Х" указывает значение, равное значению в подписке, из которой создается проводка.</span><span class="sxs-lookup"><span data-stu-id="534b3-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-109">Приоритет</span><span class="sxs-lookup"><span data-stu-id="534b3-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="534b3-110"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="534b3-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="534b3-111"><strong>Код проекта</strong></span><span class="sxs-lookup"><span data-stu-id="534b3-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="534b3-112"><strong>Подписка</strong></span><span class="sxs-lookup"><span data-stu-id="534b3-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="534b3-113"><strong>Валюта продажи</strong></span><span class="sxs-lookup"><span data-stu-id="534b3-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="534b3-114"><strong>Код периода</strong></span><span class="sxs-lookup"><span data-stu-id="534b3-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-115">1</span><span class="sxs-lookup"><span data-stu-id="534b3-115">1</span></span></p></td>
<td><p><span data-ttu-id="534b3-116">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-116">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-117">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-117">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-118">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-118">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-119">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-119">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-120">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-121">2</span><span class="sxs-lookup"><span data-stu-id="534b3-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-122">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-122">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-123">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-123">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-124">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-124">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-125">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534b3-126">3</span><span class="sxs-lookup"><span data-stu-id="534b3-126">3</span></span></p></td>
<td><p><span data-ttu-id="534b3-127">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-128">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-128">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-129">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-129">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-130">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-131">4</span><span class="sxs-lookup"><span data-stu-id="534b3-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-132">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-132">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-133">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-133">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-134">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534b3-135">5</span><span class="sxs-lookup"><span data-stu-id="534b3-135">5</span></span></p></td>
<td><p><span data-ttu-id="534b3-136">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-136">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-137">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-138">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-138">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-139">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-140">6</span><span class="sxs-lookup"><span data-stu-id="534b3-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-141">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-142">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-142">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-143">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="534b3-144">7</span><span class="sxs-lookup"><span data-stu-id="534b3-144">7</span></span></p></td>
<td><p><span data-ttu-id="534b3-145">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-146">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-146">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-147">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-148">8</span><span class="sxs-lookup"><span data-stu-id="534b3-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="534b3-149">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-149">X</span></span></p></td>
<td><p><span data-ttu-id="534b3-150">Х</span><span class="sxs-lookup"><span data-stu-id="534b3-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-151">Когда создается сбор по подписке, в качестве цены продажи подписки выбирается цена продажи с наивысшим уровнем детализации (как показано в приведенной выше таблице).</span><span class="sxs-lookup"><span data-stu-id="534b3-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="534b3-152">Обновление и индексирование цен продажи подписки</span><span class="sxs-lookup"><span data-stu-id="534b3-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="534b3-153">Можно обновить цену продажи подписки, обновив базисную цену или индекс.</span><span class="sxs-lookup"><span data-stu-id="534b3-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="534b3-154">Обновление может быть выполнено изменением на процент или до нового значения.</span><span class="sxs-lookup"><span data-stu-id="534b3-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="534b3-155">Цены продажи для сборов по подписке</span><span class="sxs-lookup"><span data-stu-id="534b3-155">Subscription fee sales prices</span></span>

<span data-ttu-id="534b3-156">Когда создается сбор по подписке, цена продажи основывается на настройке цены продажи подписки.</span><span class="sxs-lookup"><span data-stu-id="534b3-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="534b3-157">Можно использовать базисную цену из настройки цены подписки или создать индексированные цены продажи.</span><span class="sxs-lookup"><span data-stu-id="534b3-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="534b3-158">пример</span><span class="sxs-lookup"><span data-stu-id="534b3-158">Example</span></span>

<span data-ttu-id="534b3-159">Необходимо настроить цены продажи подписки в EUR 500 для нового проекта 9030.</span><span class="sxs-lookup"><span data-stu-id="534b3-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="534b3-160">В форме **Цена продажи (подписка)** можно создать строки цены продажи подписки, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="534b3-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-161">Действительно с</span><span class="sxs-lookup"><span data-stu-id="534b3-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="534b3-162">Категория</span><span class="sxs-lookup"><span data-stu-id="534b3-162">Category</span></span></p></th>
<th><p><span data-ttu-id="534b3-163">Проект</span><span class="sxs-lookup"><span data-stu-id="534b3-163">Project</span></span></p></th>
<th><p><span data-ttu-id="534b3-164">Подписка</span><span class="sxs-lookup"><span data-stu-id="534b3-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="534b3-165">Код периода</span><span class="sxs-lookup"><span data-stu-id="534b3-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="534b3-166">Валюта реализации</span><span class="sxs-lookup"><span data-stu-id="534b3-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="534b3-167">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="534b3-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="534b3-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="534b3-169">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="534b3-170">Месяц</span><span class="sxs-lookup"><span data-stu-id="534b3-170">Month</span></span></p></td>
<td><p><span data-ttu-id="534b3-171">Евро</span><span class="sxs-lookup"><span data-stu-id="534b3-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-172">500</span><span class="sxs-lookup"><span data-stu-id="534b3-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-173">Обратите внимание, что поля **Категория** и **Подписка** пусты.</span><span class="sxs-lookup"><span data-stu-id="534b3-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="534b3-174">Затем создайте следующие подписки.</span><span class="sxs-lookup"><span data-stu-id="534b3-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-175">Подписка на обслуживание</span><span class="sxs-lookup"><span data-stu-id="534b3-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="534b3-176">Проект</span><span class="sxs-lookup"><span data-stu-id="534b3-176">Project</span></span></p></th>
<th><p><span data-ttu-id="534b3-177">Группа подписок</span><span class="sxs-lookup"><span data-stu-id="534b3-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="534b3-178">Категория</span><span class="sxs-lookup"><span data-stu-id="534b3-178">Category</span></span></p></th>
<th><p><span data-ttu-id="534b3-179">Валюта</span><span class="sxs-lookup"><span data-stu-id="534b3-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="534b3-180">Код периода</span><span class="sxs-lookup"><span data-stu-id="534b3-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="534b3-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-182">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-182">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="534b3-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="534b3-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="534b3-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="534b3-185">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-186">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="534b3-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="534b3-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-188">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-188">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="534b3-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="534b3-190">СубКат2</span><span class="sxs-lookup"><span data-stu-id="534b3-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="534b3-191">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-192">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="534b3-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-193">Теперь вы создаете сборы по подписке для обеих подписок в группе подписок Sub1:</span><span class="sxs-lookup"><span data-stu-id="534b3-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="534b3-194">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.</span><span class="sxs-lookup"><span data-stu-id="534b3-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="534b3-195">В форме **Группы подписки** щелкните **Функция** \> **Создать сбор по подписке**.</span><span class="sxs-lookup"><span data-stu-id="534b3-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="534b3-196">В форме **Создание сбора по подписке** введите соответствующую информацию.</span><span class="sxs-lookup"><span data-stu-id="534b3-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="534b3-197">Дополнительные сведения см. в разделе [Создание проводок по сборам по подписке](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="534b3-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="534b3-198">Сборы по подписке с ценой продажи EUR 500 созданы для обеих подписок, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="534b3-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-199">Дата проекта</span><span class="sxs-lookup"><span data-stu-id="534b3-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="534b3-200">Подписка на обслуживание</span><span class="sxs-lookup"><span data-stu-id="534b3-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="534b3-201">Проект</span><span class="sxs-lookup"><span data-stu-id="534b3-201">Project</span></span></p></th>
<th><p><span data-ttu-id="534b3-202">Категория</span><span class="sxs-lookup"><span data-stu-id="534b3-202">Category</span></span></p></th>
<th><p><span data-ttu-id="534b3-203">Дата начала</span><span class="sxs-lookup"><span data-stu-id="534b3-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="534b3-204">Дата завершения</span><span class="sxs-lookup"><span data-stu-id="534b3-204">End date</span></span></p></th>
<th><p><span data-ttu-id="534b3-205">Валюта продаж</span><span class="sxs-lookup"><span data-stu-id="534b3-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="534b3-206">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="534b3-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="534b3-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="534b3-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="534b3-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-209">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-209">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="534b3-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="534b3-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-213">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-214">500</span><span class="sxs-lookup"><span data-stu-id="534b3-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="534b3-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="534b3-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="534b3-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-217">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-217">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-218">СубКат2</span><span class="sxs-lookup"><span data-stu-id="534b3-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="534b3-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-221">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-222">500</span><span class="sxs-lookup"><span data-stu-id="534b3-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-223">Позже вы решили, что необходимо указать цены продажи для категории SubCat1 для проекта 9030.</span><span class="sxs-lookup"><span data-stu-id="534b3-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="534b3-224">Поэтому вы создаете новую строку цены продажи с ценой продажи EUR 550 для комбинации проекта 9030 и категории SubCat1.</span><span class="sxs-lookup"><span data-stu-id="534b3-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="534b3-225">Теперь для проекта 9030 имеется две строки цены продажи подписки, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="534b3-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-226">Действительно с</span><span class="sxs-lookup"><span data-stu-id="534b3-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="534b3-227">Категория</span><span class="sxs-lookup"><span data-stu-id="534b3-227">Category</span></span></p></th>
<th><p><span data-ttu-id="534b3-228">Проект</span><span class="sxs-lookup"><span data-stu-id="534b3-228">Project</span></span></p></th>
<th><p><span data-ttu-id="534b3-229">Подписка</span><span class="sxs-lookup"><span data-stu-id="534b3-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="534b3-230">Код периода</span><span class="sxs-lookup"><span data-stu-id="534b3-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="534b3-231">Валюта</span><span class="sxs-lookup"><span data-stu-id="534b3-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="534b3-232">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="534b3-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="534b3-234">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="534b3-235">месяц</span><span class="sxs-lookup"><span data-stu-id="534b3-235">Month</span></span></p></td>
<td><p><span data-ttu-id="534b3-236">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-237">500</span><span class="sxs-lookup"><span data-stu-id="534b3-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="534b3-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="534b3-240">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="534b3-241">месяц</span><span class="sxs-lookup"><span data-stu-id="534b3-241">Month</span></span></p></td>
<td><p><span data-ttu-id="534b3-242">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-243">550</span><span class="sxs-lookup"><span data-stu-id="534b3-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-244">Вы повторяете описанную выше процедуру для создания сборов по подписке для обеих подписок в группе подписок Sub1.</span><span class="sxs-lookup"><span data-stu-id="534b3-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="534b3-245">В следующей таблице показаны проводки, созданные для каждой подписки, которая относится к группе подписок.</span><span class="sxs-lookup"><span data-stu-id="534b3-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="534b3-246">Дата проекта</span><span class="sxs-lookup"><span data-stu-id="534b3-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="534b3-247">Подписка</span><span class="sxs-lookup"><span data-stu-id="534b3-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="534b3-248">Проект</span><span class="sxs-lookup"><span data-stu-id="534b3-248">Project</span></span></p></th>
<th><p><span data-ttu-id="534b3-249">Категория</span><span class="sxs-lookup"><span data-stu-id="534b3-249">Category</span></span></p></th>
<th><p><span data-ttu-id="534b3-250">Дата начала</span><span class="sxs-lookup"><span data-stu-id="534b3-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="534b3-251">Дата завершения</span><span class="sxs-lookup"><span data-stu-id="534b3-251">End date</span></span></p></th>
<th><p><span data-ttu-id="534b3-252">Валюта продаж</span><span class="sxs-lookup"><span data-stu-id="534b3-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="534b3-253">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="534b3-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="534b3-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="534b3-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="534b3-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="534b3-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-256">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-256">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="534b3-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="534b3-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="534b3-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="534b3-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="534b3-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="534b3-260">евро</span><span class="sxs-lookup"><span data-stu-id="534b3-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-261">550</span><span class="sxs-lookup"><span data-stu-id="534b3-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="534b3-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="534b3-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="534b3-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="534b3-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="534b3-264">9030</span><span class="sxs-lookup"><span data-stu-id="534b3-264">9030</span></span></p></td>
<td><p><span data-ttu-id="534b3-265">СубКат2</span><span class="sxs-lookup"><span data-stu-id="534b3-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="534b3-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="534b3-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="534b3-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="534b3-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="534b3-268">Евро</span><span class="sxs-lookup"><span data-stu-id="534b3-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="534b3-269">500</span><span class="sxs-lookup"><span data-stu-id="534b3-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="534b3-270">В первой проводке для подписки 00020\_135 цена продажи EUR 550 извлекается из цены продажи подписки, настроенной для комбинации конкретного проекта и категории.</span><span class="sxs-lookup"><span data-stu-id="534b3-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="534b3-271">Во второй проводке для подписки 00021\_135 в качестве цены продажи подписки для проекта используется цена продажи 500, поскольку для комбинации проекта 9030 и категории SubCat2 не настроена цена.</span><span class="sxs-lookup"><span data-stu-id="534b3-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="534b3-272">См. также</span><span class="sxs-lookup"><span data-stu-id="534b3-272">See also</span></span>

[<span data-ttu-id="534b3-273">Обновление и индексирование цен продажи подписки</span><span class="sxs-lookup"><span data-stu-id="534b3-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]