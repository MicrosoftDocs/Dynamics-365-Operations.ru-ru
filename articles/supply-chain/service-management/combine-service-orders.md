---
title: Объединение заказов на сервисное обслуживание
description: Можно объединить заказы на сервисное обслуживание.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "311872"
---
# <a name="combine-service-orders"></a><span data-ttu-id="de7ae-103">Объединение заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="de7ae-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="de7ae-104">При автоматическом создании строк заказа на сервисное обслуживание в форме **Соглашения о сервисном обслуживании** можно выбрать один из следующих вариантов их группирования:</span><span class="sxs-lookup"><span data-stu-id="de7ae-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="de7ae-105">**По соглашению о сервисном обслуживании**</span><span class="sxs-lookup"><span data-stu-id="de7ae-105">**By service agreement**</span></span>

  - <span data-ttu-id="de7ae-106">**По задачам сервисного обслуживания**</span><span class="sxs-lookup"><span data-stu-id="de7ae-106">**By service task**</span></span>

  - <span data-ttu-id="de7ae-107">**По сотрудникам**</span><span class="sxs-lookup"><span data-stu-id="de7ae-107">**By employee**</span></span>

  - <span data-ttu-id="de7ae-108">**По объектам сервисного обслуживания**</span><span class="sxs-lookup"><span data-stu-id="de7ae-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="de7ae-109">Пример</span><span class="sxs-lookup"><span data-stu-id="de7ae-109">Example</span></span>

<span data-ttu-id="de7ae-110">Вы создаете соглашение о сервисном обслуживание с начальной датой 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="de7ae-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="de7ae-111">В поле **Объединение заказов на сервисное обслуживание** выберите **По объектам сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="de7ae-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="de7ae-112">После этого создаются следующие строки соглашения на обслуживание:</span><span class="sxs-lookup"><span data-stu-id="de7ae-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="de7ae-113">Номер строки договора</span><span class="sxs-lookup"><span data-stu-id="de7ae-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="de7ae-114">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="de7ae-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="de7ae-115">описание</span><span class="sxs-lookup"><span data-stu-id="de7ae-115">Description</span></span></p></th>
<th><p><span data-ttu-id="de7ae-116">Интервал</span><span class="sxs-lookup"><span data-stu-id="de7ae-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="de7ae-117">Объект сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="de7ae-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="de7ae-118">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="de7ae-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de7ae-119">1</span><span class="sxs-lookup"><span data-stu-id="de7ae-119">1</span></span></p></td>
<td><p><span data-ttu-id="de7ae-120"><strong>Часы</strong></span><span class="sxs-lookup"><span data-stu-id="de7ae-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de7ae-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="de7ae-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="de7ae-122">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="de7ae-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="de7ae-123">X-1</span><span class="sxs-lookup"><span data-stu-id="de7ae-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="de7ae-124">04-01-2007</span><span class="sxs-lookup"><span data-stu-id="de7ae-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de7ae-125">2</span><span class="sxs-lookup"><span data-stu-id="de7ae-125">2</span></span></p></td>
<td><p><span data-ttu-id="de7ae-126"><strong>Часы</strong></span><span class="sxs-lookup"><span data-stu-id="de7ae-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de7ae-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="de7ae-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="de7ae-128">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="de7ae-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="de7ae-129">X-2</span><span class="sxs-lookup"><span data-stu-id="de7ae-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="de7ae-130">04-01-2007</span><span class="sxs-lookup"><span data-stu-id="de7ae-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de7ae-131">3</span><span class="sxs-lookup"><span data-stu-id="de7ae-131">3</span></span></p></td>
<td><p><span data-ttu-id="de7ae-132"><strong>Часы</strong></span><span class="sxs-lookup"><span data-stu-id="de7ae-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de7ae-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="de7ae-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="de7ae-134">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="de7ae-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="de7ae-135">X-2</span><span class="sxs-lookup"><span data-stu-id="de7ae-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="de7ae-136">04-01-2007</span><span class="sxs-lookup"><span data-stu-id="de7ae-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de7ae-137">Окна времени для любой из строк соглашения на обслуживание не указаны.</span><span class="sxs-lookup"><span data-stu-id="de7ae-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="de7ae-138">Поэтому строки заказа на сервисное обслуживание не будут сдвигаться с того расчетного дня, на который они выпадают.</span><span class="sxs-lookup"><span data-stu-id="de7ae-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="de7ae-139">Затем создаются строки заказа на обслуживание в форме **Create service orders** с 04-01-2007 по 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="de7ae-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="de7ae-140">Всего создается 10 заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="de7ae-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="de7ae-141">Поскольку была выбрана настройка объединения **По объектам сервисного обслуживания**, все созданные заказы на обслуживание имеют только строки, относящиеся к одному конкретному объекту обслуживания.</span><span class="sxs-lookup"><span data-stu-id="de7ae-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="de7ae-142">Строки заказа на сервисное обслуживание, которые создаются из соглашения о сервисном обслуживании и имеют одинаковые дату и объект обслуживания, объединяются в одном и том же заказе на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="de7ae-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de7ae-143">В этом примере календарь, указанный в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG>, не имеет закрытых дней.</span><span class="sxs-lookup"><span data-stu-id="de7ae-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="de7ae-144">Дополнительное группирование строк заказа на сервисное обслуживание в заказы на сервисное обслуживание происходит в соответствии с произвольным окном времени, указанным в строках соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="de7ae-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="de7ae-145">См. также</span><span class="sxs-lookup"><span data-stu-id="de7ae-145">See also</span></span>

[<span data-ttu-id="de7ae-146">Автоматическое создание заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="de7ae-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


