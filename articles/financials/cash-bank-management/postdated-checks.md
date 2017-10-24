---
title: "Чеки, датированные будущим числом"
description: "Эта статья содержит сведения о поддержке чеков, датированных будущим числом, в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Чеки, датированные будущим числом, выпускаются для создания и получения платежей в будущем. Поэтому чек нельзя обналичить до указанной даты."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a535b5f1192b7c27383cb8ece53f76a9c76f047
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="postdated-checks"></a><span data-ttu-id="1a927-105">Чеки, датированные будущим числом</span><span class="sxs-lookup"><span data-stu-id="1a927-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1a927-106">Эта статья содержит сведения о поддержке чеков, датированных будущим числом, в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="1a927-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="1a927-107">Чеки, датированные будущим числом, выпускаются для создания и получения платежей в будущем.</span><span class="sxs-lookup"><span data-stu-id="1a927-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="1a927-108">Поэтому чек нельзя обналичить до указанной даты.</span><span class="sxs-lookup"><span data-stu-id="1a927-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="1a927-109">Microsoft Dynamics 365 for Finance and Operations поддерживает полный цикл управления для чеков, датированных задним числом, как в расчетах с клиентами, так и расчетах с поставщиками, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1a927-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a927-110">Сценарий</span><span class="sxs-lookup"><span data-stu-id="1a927-110">Scenario</span></span></th>
<th><span data-ttu-id="1a927-111">Подробности</span><span class="sxs-lookup"><span data-stu-id="1a927-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a927-112">Настройка датированных задним числом чеков</span><span class="sxs-lookup"><span data-stu-id="1a927-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="1a927-113">Необходимо настроить новый способ оплаты и определить процедуры платежа для клиринговых счетов для выписанные чеки, полученные чеки и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="1a927-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a927-114">Регистрация и разнесение датированного задним числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="1a927-115">Регистрация сведений о датированном будущим числом чека, который поставщику выписывается.</span><span class="sxs-lookup"><span data-stu-id="1a927-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="1a927-116">При разноске платежа задолженность поставщику распознается, но банковский счет еще не кредитуется.</span><span class="sxs-lookup"><span data-stu-id="1a927-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="1a927-117">Вместо этого клиринговый счет используется для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1a927-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a927-118">Регистрация и разноска датированного будущим числом чека для клиента</span><span class="sxs-lookup"><span data-stu-id="1a927-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="1a927-119">Регистрация информации о полученных от клиентов чеках, датированных будущим числом.</span><span class="sxs-lookup"><span data-stu-id="1a927-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="1a927-120">При разноске платежа сумма с клиента кредитуется, но банковский счет еще не дебетуется.</span><span class="sxs-lookup"><span data-stu-id="1a927-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="1a927-121">Вместо этого клиринговый счет используется для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1a927-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a927-122">Регистрация и разнесение датированного будущим числом чека для клиента или поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="1a927-123">Если исходный чек для поставщика или от клиента поврежден или потерян, можно выпустить заменяющий чек, датированный будущим числом.</span><span class="sxs-lookup"><span data-stu-id="1a927-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="1a927-124">При регистрации сведений о чеке необходимо сослаться на исходный чек и указать, что новый чек является заменой исходного чека.</span><span class="sxs-lookup"><span data-stu-id="1a927-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="1a927-125">Также можно разнести заменяющий чек.</span><span class="sxs-lookup"><span data-stu-id="1a927-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a927-126">Перенос датированного задним числом чека клиента поставщику</span><span class="sxs-lookup"><span data-stu-id="1a927-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="1a927-127">При получении чека, датированного будущим числом, от клиента, можно передать этот чек поставщику в качестве оплаты.</span><span class="sxs-lookup"><span data-stu-id="1a927-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a927-128">Сопоставление датированного задним числом чека для клиента или поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="1a927-129">Сопоставляйте чека, датированного будущим числом, разнесенного на Промежуточный счет для клиента или поставщика, когда чек начнет действовать.</span><span class="sxs-lookup"><span data-stu-id="1a927-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="1a927-130">Когда чек сопоставлен, банк наконец дебетует или кредитует относительно клирингового счета, который был использован ранее.</span><span class="sxs-lookup"><span data-stu-id="1a927-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a927-131">Отмена датированного задним числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="1a927-132">Разнесенный чек, датированный будущим числом, можно отменить в следующих случаях: — Чек возвращен банком.</span><span class="sxs-lookup"><span data-stu-id="1a927-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="1a927-133">- Чек применен к неправильной накладной.</span><span class="sxs-lookup"><span data-stu-id="1a927-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="1a927-134">- По чему произведена наличная оплата.</span><span class="sxs-lookup"><span data-stu-id="1a927-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a927-135">Остановка платежа по датированному будущим числом чеку</span><span class="sxs-lookup"><span data-stu-id="1a927-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="1a927-136">Можно остановить платеж по выписанному задним числом чеку, выписанному поставщику, в случае недостатка средств, изменения условий соглашения с поставщиком, поставки дефектных товаров поставщиком или возврата товаров поставщику.</span><span class="sxs-lookup"><span data-stu-id="1a927-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="1a927-137">Остановить платеж можно только по чекам, которые еще не были проведены в системе.</span><span class="sxs-lookup"><span data-stu-id="1a927-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1a927-138">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1a927-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="1a927-139">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="1a927-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="1a927-140">Регистрация и разноска датированного будущим числом чека для клиента</span><span class="sxs-lookup"><span data-stu-id="1a927-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="1a927-141">Сопоставление датированного будущим числом чека от клиента</span><span class="sxs-lookup"><span data-stu-id="1a927-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="1a927-142">Регистрация и разноска датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="1a927-143">Сопоставление датированного будущим числом чека для поставщика</span><span class="sxs-lookup"><span data-stu-id="1a927-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




