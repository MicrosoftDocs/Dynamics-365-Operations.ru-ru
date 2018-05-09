---
title: "Графики поставки"
description: "Графики поставки позволяют отслеживать количество в строках заказа при использовании нескольких поставок для одного заказа на продажу, предложения по продажам или заказа на покупку."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5e48d8f0ec434acdcfb72a38ccbf8dbc6938a256
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="delivery-schedules"></a><span data-ttu-id="ae599-103">Графики поставки</span><span class="sxs-lookup"><span data-stu-id="ae599-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae599-104">Графики поставки позволяют отслеживать количество в строках заказа при использовании нескольких поставок для одного заказа на продажу, предложения по продажам или заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ae599-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="ae599-105">Используйте график поставки, когда полное количество в строке заказа или предложения необходимо поставить в нескольких отгрузках.</span><span class="sxs-lookup"><span data-stu-id="ae599-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="ae599-106">Индивидуальные отгрузки представлены строками поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="ae599-107">Два или более строки поставки составляют один график поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="ae599-108">В строках поставки могут быть указаны различные даты, количества и способы поставки или аналитики хранения, такие как сайт и склад.</span><span class="sxs-lookup"><span data-stu-id="ae599-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="ae599-109">**Пример графика поставки**</span><span class="sxs-lookup"><span data-stu-id="ae599-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="ae599-110">Итоговый заказ (исходная строка заказа)</span><span class="sxs-lookup"><span data-stu-id="ae599-110">Total order (original order line)</span></span> | <span data-ttu-id="ae599-111">600 стульев</span><span class="sxs-lookup"><span data-stu-id="ae599-111">600 chairs</span></span>                               |
| <span data-ttu-id="ae599-112">Запрошенный график поставки</span><span class="sxs-lookup"><span data-stu-id="ae599-112">Requested delivery schedule</span></span>       | <span data-ttu-id="ae599-113">100 стульев в месяц</span><span class="sxs-lookup"><span data-stu-id="ae599-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="ae599-114">Запрошенные временные рамки для поставки</span><span class="sxs-lookup"><span data-stu-id="ae599-114">Requested time frame for delivery</span></span> | <span data-ttu-id="ae599-115">6 месяцев, по первым числам каждого месяца</span><span class="sxs-lookup"><span data-stu-id="ae599-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="ae599-116">В этом случае клиент запрашивает поставку 600 стульев группами по 100 стульев в течение шести месяцев.</span><span class="sxs-lookup"><span data-stu-id="ae599-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="ae599-117">Чтобы отслеживать требования поставки вы создаете график поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="ae599-118">На странице графика поставки создается шесть отдельных строк поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="ae599-119">Каждая строка поставки содержит 100 стульев и отображает даты поставки для этих 100 стульев.</span><span class="sxs-lookup"><span data-stu-id="ae599-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="ae599-120">В этом случае каждая строка смещается на первый день месяца в течение шести последовательных месяцев.</span><span class="sxs-lookup"><span data-stu-id="ae599-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="ae599-121">Когда вы создаете график поставки, тип строки первоначального заказа автоматически изменяется на **Строка заказа с множественными поставками**.</span><span class="sxs-lookup"><span data-stu-id="ae599-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="ae599-122">Строка этого типа называется коммерческой строкой и отмечена значком.</span><span class="sxs-lookup"><span data-stu-id="ae599-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="ae599-123">Строка поставки отмечена другим значком.</span><span class="sxs-lookup"><span data-stu-id="ae599-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="ae599-124">Если вы изменяете количество в строке поставки, коммерческая строка обновляется до полного количества графика поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="ae599-125">Если торговое соглашение определило полную скидку для заказа, то график поставки обеспечивает, что для вашего заказа действует полная скидка по заказу, даже если заказ разделен на несколько поставок.</span><span class="sxs-lookup"><span data-stu-id="ae599-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="ae599-126">Заказы, которые имеют график поставки, обрабатываются по строкам поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="ae599-127">Обработка включает разноску отборочных накладных, поступлений продуктов и выставление накладных.</span><span class="sxs-lookup"><span data-stu-id="ae599-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="ae599-128">Документальные распечатки заказов и предложений, которые имеют график поставки, содержат только строки поставки.</span><span class="sxs-lookup"><span data-stu-id="ae599-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="ae599-129">В них не отображаются исходные строки (коммерческие строки).</span><span class="sxs-lookup"><span data-stu-id="ae599-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="ae599-130">**Примечание.** Кроме того, только строки поставки отображаются, когда вы выполняете следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ae599-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="ae599-131">Разнести</span><span class="sxs-lookup"><span data-stu-id="ae599-131">Post</span></span>
-   <span data-ttu-id="ae599-132">Копирование страниц</span><span class="sxs-lookup"><span data-stu-id="ae599-132">Copy pages</span></span>
-   <span data-ttu-id="ae599-133">Просмотр страниц списков и отчетов</span><span class="sxs-lookup"><span data-stu-id="ae599-133">Browse list pages and reports</span></span>

<span data-ttu-id="ae599-134">После подтверждения предложений по продажам в итоговых заказах на покупку отображается весь график поставки, включая даже строки заказа с несколькими поставками.</span><span class="sxs-lookup"><span data-stu-id="ae599-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="ae599-135">Кроме того, весь график поставки отображается на всех основных страницах, таких как заказы на продажу, предложения по продажам и заказы на покупку.</span><span class="sxs-lookup"><span data-stu-id="ae599-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




