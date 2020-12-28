---
title: Определение порядка списания возврата
description: Определение порядка списания возврата.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2b1468328433a67253bafc21ac9c9b3a2398872
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435707"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="589fa-103">Определение порядка списания возврата</span><span class="sxs-lookup"><span data-stu-id="589fa-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="589fa-104">При обработке заказа на возврат следует указать код причины, чтобы определить, почему продукт возвращается.</span><span class="sxs-lookup"><span data-stu-id="589fa-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="589fa-105">Необходимо также указать код расстановки и действие метода обработки, чтобы указать, что следует сделать с возвращаемым продуктом.</span><span class="sxs-lookup"><span data-stu-id="589fa-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="589fa-106">Код метода обработки может применяться при создании заказа на возврат, регистрации прибытия номенклатуры или обновления отборочных накладных при прибытии номенклатуры и завершения карантинного заказа.</span><span class="sxs-lookup"><span data-stu-id="589fa-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="589fa-107">Можно определить коды методов обработки, которые необходимы для поддержки бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="589fa-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="589fa-108">В следующей таблице представлено множество обычно используемых кодов для назначения методов обработки возвращаемого элемента номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="589fa-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="589fa-109">Тип метода обработки</span><span class="sxs-lookup"><span data-stu-id="589fa-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="589fa-110">Общий код</span><span class="sxs-lookup"><span data-stu-id="589fa-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="589fa-111">Описание</span><span class="sxs-lookup"><span data-stu-id="589fa-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="589fa-112">Выбытие</span><span class="sxs-lookup"><span data-stu-id="589fa-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="589fa-113">SC</span><span class="sxs-lookup"><span data-stu-id="589fa-113">SC</span></span></p></td>
<td><p><span data-ttu-id="589fa-114">Отходы/уничтожение</span><span class="sxs-lookup"><span data-stu-id="589fa-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-115">Выбытие</span><span class="sxs-lookup"><span data-stu-id="589fa-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="589fa-116">DC</span><span class="sxs-lookup"><span data-stu-id="589fa-116">DC</span></span></p></td>
<td><p><span data-ttu-id="589fa-117">Благотворительные пожертвования</span><span class="sxs-lookup"><span data-stu-id="589fa-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-118">Выбытие</span><span class="sxs-lookup"><span data-stu-id="589fa-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="589fa-119">TD</span><span class="sxs-lookup"><span data-stu-id="589fa-119">TD</span></span></p></td>
<td><p><span data-ttu-id="589fa-120">Утилизация третьих сторон</span><span class="sxs-lookup"><span data-stu-id="589fa-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-121">Выбытие</span><span class="sxs-lookup"><span data-stu-id="589fa-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="589fa-122">SL</span><span class="sxs-lookup"><span data-stu-id="589fa-122">SL</span></span></p></td>
<td><p><span data-ttu-id="589fa-123">Ликвидация</span><span class="sxs-lookup"><span data-stu-id="589fa-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-124">Выбытие</span><span class="sxs-lookup"><span data-stu-id="589fa-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="589fa-125">TS</span><span class="sxs-lookup"><span data-stu-id="589fa-125">TS</span></span></p></td>
<td><p><span data-ttu-id="589fa-126">Продажи третьих лиц (вторичные рынки)</span><span class="sxs-lookup"><span data-stu-id="589fa-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-127">Ремонт/модификация</span><span class="sxs-lookup"><span data-stu-id="589fa-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="589fa-128">RW</span><span class="sxs-lookup"><span data-stu-id="589fa-128">RW</span></span></p></td>
<td><p><span data-ttu-id="589fa-129">Доработка</span><span class="sxs-lookup"><span data-stu-id="589fa-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-130">Ремонт/модификация</span><span class="sxs-lookup"><span data-stu-id="589fa-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="589fa-131">RF</span><span class="sxs-lookup"><span data-stu-id="589fa-131">RF</span></span></p></td>
<td><p><span data-ttu-id="589fa-132">Повторное изготовление/Восстановление</span><span class="sxs-lookup"><span data-stu-id="589fa-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-133">Ремонт/модификация</span><span class="sxs-lookup"><span data-stu-id="589fa-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="589fa-134">MD</span><span class="sxs-lookup"><span data-stu-id="589fa-134">MD</span></span></p></td>
<td><p><span data-ttu-id="589fa-135">Изменить</span><span class="sxs-lookup"><span data-stu-id="589fa-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-136">Ремонт/модификация</span><span class="sxs-lookup"><span data-stu-id="589fa-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="589fa-137">RP</span><span class="sxs-lookup"><span data-stu-id="589fa-137">RP</span></span></p></td>
<td><p><span data-ttu-id="589fa-138">Ремонт</span><span class="sxs-lookup"><span data-stu-id="589fa-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-139">Ремонт/модификация</span><span class="sxs-lookup"><span data-stu-id="589fa-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="589fa-140">RV</span><span class="sxs-lookup"><span data-stu-id="589fa-140">RV</span></span></p></td>
<td><p><span data-ttu-id="589fa-141">Возврат поставщику</span><span class="sxs-lookup"><span data-stu-id="589fa-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-142">Прочее</span><span class="sxs-lookup"><span data-stu-id="589fa-142">Other</span></span></p></td>
<td><p><span data-ttu-id="589fa-143">AI</span><span class="sxs-lookup"><span data-stu-id="589fa-143">AI</span></span></p></td>
<td><p><span data-ttu-id="589fa-144">Использовать "как есть"</span><span class="sxs-lookup"><span data-stu-id="589fa-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-145">Прочее</span><span class="sxs-lookup"><span data-stu-id="589fa-145">Other</span></span></p></td>
<td><p><span data-ttu-id="589fa-146">RS</span><span class="sxs-lookup"><span data-stu-id="589fa-146">RS</span></span></p></td>
<td><p><span data-ttu-id="589fa-147">Перепродажа</span><span class="sxs-lookup"><span data-stu-id="589fa-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-148">Прочее</span><span class="sxs-lookup"><span data-stu-id="589fa-148">Other</span></span></p></td>
<td><p><span data-ttu-id="589fa-149">EX</span><span class="sxs-lookup"><span data-stu-id="589fa-149">EX</span></span></p></td>
<td><p><span data-ttu-id="589fa-150">Биржа</span><span class="sxs-lookup"><span data-stu-id="589fa-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-151">Прочее</span><span class="sxs-lookup"><span data-stu-id="589fa-151">Other</span></span></p></td>
<td><p><span data-ttu-id="589fa-152">MS</span><span class="sxs-lookup"><span data-stu-id="589fa-152">MS</span></span></p></td>
<td><p><span data-ttu-id="589fa-153">Разное</span><span class="sxs-lookup"><span data-stu-id="589fa-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="589fa-154">Для каждого кода расстановки, который вы определяете, необходимо выбрать действие метода обработки.</span><span class="sxs-lookup"><span data-stu-id="589fa-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="589fa-155">Действие метода обработки определяет физические и финансовые последствия кодов расстановки.</span><span class="sxs-lookup"><span data-stu-id="589fa-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="589fa-156">Например, действие метода обработки определяет физическую обработку возвращенной номенклатуры, финансовые последствия возврата номенклатуры, и необходимость отправки заменяющей номенклатуры клиенту.</span><span class="sxs-lookup"><span data-stu-id="589fa-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="589fa-157">Можно определить неограниченное количество кодов расстановки согласно вашим бизнес-потребностям, но есть только шесть предопределенных действия метода обработки, которые можно выбирать.</span><span class="sxs-lookup"><span data-stu-id="589fa-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="589fa-158">В приведенной ниже таблице показаны действия метода обработки и их определения.</span><span class="sxs-lookup"><span data-stu-id="589fa-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="589fa-159">Действие метода обработки</span><span class="sxs-lookup"><span data-stu-id="589fa-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="589fa-160">описание</span><span class="sxs-lookup"><span data-stu-id="589fa-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="589fa-161"><strong>По кредиту</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-162">Возврат номенклатуры на склад и кредитование клиента.</span><span class="sxs-lookup"><span data-stu-id="589fa-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-163"><strong>Только по кредиту</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-164">Кредитование клиента без необходимости или ожидания возврата номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="589fa-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-165"><strong>Отходы</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-166">Отбраковка номенклатуру и кредитование клиента.</span><span class="sxs-lookup"><span data-stu-id="589fa-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-167"><strong>Заменить и кредитовать</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-168">Возврат номенклатуры на склад, создание заказа на замену и кредитование клиента.</span><span class="sxs-lookup"><span data-stu-id="589fa-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589fa-169"><strong>Заменить и списать в отходы</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-170">Отбраковки номенклатуры, создание заказа на замену и кредитование клиента.</span><span class="sxs-lookup"><span data-stu-id="589fa-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589fa-171"><strong>Вернуть клиенту</strong></span><span class="sxs-lookup"><span data-stu-id="589fa-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="589fa-172">Отклонение возвращенной номенклатуры и возврат ее клиенту.</span><span class="sxs-lookup"><span data-stu-id="589fa-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="589fa-173">Выберите код метода обработки для карантинного заказа</span><span class="sxs-lookup"><span data-stu-id="589fa-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="589fa-174">Щелкните **Управление запасами** \> **Периодические операции** \> **Управление качеством** \> **Карантинные заказы**.</span><span class="sxs-lookup"><span data-stu-id="589fa-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="589fa-175">Для существующего карантинного заказа выберите действие из поля **Код метода обработки** на вкладке **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="589fa-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="589fa-176">См. также</span><span class="sxs-lookup"><span data-stu-id="589fa-176">See also</span></span>

<span data-ttu-id="589fa-177">[Карантинный заказ (форма)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="589fa-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="589fa-178">[Коды методов обработки (форма)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="589fa-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  


