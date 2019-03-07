---
title: Пример дней сокращения
description: Пример дней сокращения.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "334113"
---
# <a name="reduction-days-example"></a><span data-ttu-id="dbe1f-103">Пример дней сокращения</span><span class="sxs-lookup"><span data-stu-id="dbe1f-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dbe1f-104">Вы создали проводку по подписке клиента на обслуживание, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="dbe1f-105">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="dbe1f-105">From date</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-106">До даты</span><span class="sxs-lookup"><span data-stu-id="dbe1f-106">To date</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-107">Подписка</span><span class="sxs-lookup"><span data-stu-id="dbe1f-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-108">Тип подписки</span><span class="sxs-lookup"><span data-stu-id="dbe1f-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-109">Project</span><span class="sxs-lookup"><span data-stu-id="dbe1f-109">Project</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-110">Категория</span><span class="sxs-lookup"><span data-stu-id="dbe1f-110">Category</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-111">Валюта реализации</span><span class="sxs-lookup"><span data-stu-id="dbe1f-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-112">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="dbe1f-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbe1f-113">01 марта 2011</span><span class="sxs-lookup"><span data-stu-id="dbe1f-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-114">31 марта 2011</span><span class="sxs-lookup"><span data-stu-id="dbe1f-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="dbe1f-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-116"><strong>Периодически</strong></span><span class="sxs-lookup"><span data-stu-id="dbe1f-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="dbe1f-117">9013</span><span class="sxs-lookup"><span data-stu-id="dbe1f-117">9013</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-118">СубКат2</span><span class="sxs-lookup"><span data-stu-id="dbe1f-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-119">Евро</span><span class="sxs-lookup"><span data-stu-id="dbe1f-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-120">200,00</span><span class="sxs-lookup"><span data-stu-id="dbe1f-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbe1f-121">Клиент уведомил, что в течение двух дней (10 и 11 марта) сервисное обслуживание не потребуется.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="dbe1f-122">Вы соглашаетесь уменьшить подписку на эти два дня.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="dbe1f-123">Вы создаете новую проводку типа **Дни сокращения**, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="dbe1f-124">с даты</span><span class="sxs-lookup"><span data-stu-id="dbe1f-124">From date</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-125">До даты</span><span class="sxs-lookup"><span data-stu-id="dbe1f-125">To date</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-126">Подписка</span><span class="sxs-lookup"><span data-stu-id="dbe1f-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-127">Тип подписки</span><span class="sxs-lookup"><span data-stu-id="dbe1f-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-128">Project</span><span class="sxs-lookup"><span data-stu-id="dbe1f-128">Project</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-129">Категория</span><span class="sxs-lookup"><span data-stu-id="dbe1f-129">Category</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-130">Валюта реализации</span><span class="sxs-lookup"><span data-stu-id="dbe1f-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="dbe1f-131">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="dbe1f-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbe1f-132">10 марта 2011</span><span class="sxs-lookup"><span data-stu-id="dbe1f-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-133">11 марта 2011</span><span class="sxs-lookup"><span data-stu-id="dbe1f-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="dbe1f-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-135"><strong>Дни сокращения</strong></span><span class="sxs-lookup"><span data-stu-id="dbe1f-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="dbe1f-136">9013</span><span class="sxs-lookup"><span data-stu-id="dbe1f-136">9013</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-137">СубКат2</span><span class="sxs-lookup"><span data-stu-id="dbe1f-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-138">Евро</span><span class="sxs-lookup"><span data-stu-id="dbe1f-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="dbe1f-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="dbe1f-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dbe1f-140">При выставлении счета за операции марта 2011 года цена продажи евро 200 уменьшается на сумму 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="dbe1f-141">Сумма к оплате за операцию по подписке составляет, таким образом, 187,10 EUR, и по двум операциям выставляется счет на общую сумму 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe1f-142">См. также</span><span class="sxs-lookup"><span data-stu-id="dbe1f-142">See also</span></span>

[<span data-ttu-id="dbe1f-143">Уменьшение дней в сборах по подписке</span><span class="sxs-lookup"><span data-stu-id="dbe1f-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


