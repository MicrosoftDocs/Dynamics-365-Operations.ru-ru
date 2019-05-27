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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564516"
---
# <a name="reduction-days-example"></a><span data-ttu-id="8f415-103">Пример дней сокращения</span><span class="sxs-lookup"><span data-stu-id="8f415-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8f415-104">Вы создали проводку по подписке клиента на обслуживание, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8f415-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8f415-105">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="8f415-105">From date</span></span></p></th>
<th><p><span data-ttu-id="8f415-106">До даты</span><span class="sxs-lookup"><span data-stu-id="8f415-106">To date</span></span></p></th>
<th><p><span data-ttu-id="8f415-107">Подписка</span><span class="sxs-lookup"><span data-stu-id="8f415-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8f415-108">Тип подписки</span><span class="sxs-lookup"><span data-stu-id="8f415-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8f415-109">Project</span><span class="sxs-lookup"><span data-stu-id="8f415-109">Project</span></span></p></th>
<th><p><span data-ttu-id="8f415-110">Категория</span><span class="sxs-lookup"><span data-stu-id="8f415-110">Category</span></span></p></th>
<th><p><span data-ttu-id="8f415-111">Валюта реализации</span><span class="sxs-lookup"><span data-stu-id="8f415-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8f415-112">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="8f415-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f415-113">01 марта 2011</span><span class="sxs-lookup"><span data-stu-id="8f415-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="8f415-114">31 марта 2011</span><span class="sxs-lookup"><span data-stu-id="8f415-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="8f415-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="8f415-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8f415-116"><strong>Периодически</strong></span><span class="sxs-lookup"><span data-stu-id="8f415-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="8f415-117">9013</span><span class="sxs-lookup"><span data-stu-id="8f415-117">9013</span></span></p></td>
<td><p><span data-ttu-id="8f415-118">СубКат2</span><span class="sxs-lookup"><span data-stu-id="8f415-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8f415-119">Евро</span><span class="sxs-lookup"><span data-stu-id="8f415-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="8f415-120">200,00</span><span class="sxs-lookup"><span data-stu-id="8f415-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f415-121">Клиент уведомил, что в течение двух дней (10 и 11 марта) сервисное обслуживание не потребуется.</span><span class="sxs-lookup"><span data-stu-id="8f415-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="8f415-122">Вы соглашаетесь уменьшить подписку на эти два дня.</span><span class="sxs-lookup"><span data-stu-id="8f415-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="8f415-123">Вы создаете новую проводку типа **Дни сокращения**, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8f415-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8f415-124">с даты</span><span class="sxs-lookup"><span data-stu-id="8f415-124">From date</span></span></p></th>
<th><p><span data-ttu-id="8f415-125">До даты</span><span class="sxs-lookup"><span data-stu-id="8f415-125">To date</span></span></p></th>
<th><p><span data-ttu-id="8f415-126">Подписка</span><span class="sxs-lookup"><span data-stu-id="8f415-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8f415-127">Тип подписки</span><span class="sxs-lookup"><span data-stu-id="8f415-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8f415-128">Project</span><span class="sxs-lookup"><span data-stu-id="8f415-128">Project</span></span></p></th>
<th><p><span data-ttu-id="8f415-129">Категория</span><span class="sxs-lookup"><span data-stu-id="8f415-129">Category</span></span></p></th>
<th><p><span data-ttu-id="8f415-130">Валюта реализации</span><span class="sxs-lookup"><span data-stu-id="8f415-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8f415-131">Цена продажи</span><span class="sxs-lookup"><span data-stu-id="8f415-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f415-132">10 марта 2011</span><span class="sxs-lookup"><span data-stu-id="8f415-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="8f415-133">11 марта 2011</span><span class="sxs-lookup"><span data-stu-id="8f415-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="8f415-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="8f415-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8f415-135"><strong>Дни сокращения</strong></span><span class="sxs-lookup"><span data-stu-id="8f415-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="8f415-136">9013</span><span class="sxs-lookup"><span data-stu-id="8f415-136">9013</span></span></p></td>
<td><p><span data-ttu-id="8f415-137">СубКат2</span><span class="sxs-lookup"><span data-stu-id="8f415-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8f415-138">Евро</span><span class="sxs-lookup"><span data-stu-id="8f415-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="8f415-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="8f415-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f415-140">При выставлении счета за операции марта 2011 года цена продажи евро 200 уменьшается на сумму 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="8f415-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="8f415-141">Сумма к оплате за операцию по подписке составляет, таким образом, 187,10 EUR, и по двум операциям выставляется счет на общую сумму 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="8f415-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f415-142">См. также</span><span class="sxs-lookup"><span data-stu-id="8f415-142">See also</span></span>

[<span data-ttu-id="8f415-143">Уменьшение дней в сборах по подписке</span><span class="sxs-lookup"><span data-stu-id="8f415-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


