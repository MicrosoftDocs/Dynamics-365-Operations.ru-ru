---
title: "Обзор управления транспортировкой"
description: "В этом разделе представлен обзор функций управления транспортировкой в Microsoft Dynamics 365 for Finance and Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1c71c8f6c4f94342ac18cbfb7dfbc02ddb3f9f35
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="transportation-management-overview"></a><span data-ttu-id="519c8-103">Обзор управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="519c8-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="519c8-104">В этом разделе представлен обзор функций управления транспортировкой в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="519c8-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="519c8-105">Модуль "Управление транспортировкой" позволяет использовать транспорт вашей компании, а также определять поставщиков и маршрутные решения для входящих и исходящих заказов.</span><span class="sxs-lookup"><span data-stu-id="519c8-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="519c8-106">Например, можно определить самый быстрый маршрут или наименьшую ставку для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="519c8-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="519c8-107">Следующая таблица содержит описание основных сценариев использования модуля "Управление транспортировкой" в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="519c8-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="519c8-108">Сценарий</span><span class="sxs-lookup"><span data-stu-id="519c8-108">Scenario</span></span></th>
<th><span data-ttu-id="519c8-109">Как может помочь модуль «Управление транспортировкой»</span><span class="sxs-lookup"><span data-stu-id="519c8-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="519c8-110">Использование внешних поставщиков логистики для мероприятий по транспортировке.</span><span class="sxs-lookup"><span data-stu-id="519c8-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="519c8-111">Использование модуля «Управление транспортировкой» для входящей и/или исходящей транспортировки.</span><span class="sxs-lookup"><span data-stu-id="519c8-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="519c8-112">Собственный флот компании доступен для доставки/отправки, и расходы поставки переносятся на клиентов.</span><span class="sxs-lookup"><span data-stu-id="519c8-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="519c8-113">Для исходящих процессов можно использовать модуль «Управление транспортировкой» для определения расходов на транспортировку и переноса этих расходов на клиентов.</span><span class="sxs-lookup"><span data-stu-id="519c8-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="519c8-114">Однако процесс сверки накладных перевозчика не требуется.</span><span class="sxs-lookup"><span data-stu-id="519c8-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="519c8-115">Собственный флот компании доступен для доставки/отправки, но расходы поставки не переносятся на клиентов, поскольку цены продукта включают транспортировку.</span><span class="sxs-lookup"><span data-stu-id="519c8-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="519c8-116">Большая часть функций модуля «Управление транспортировкой» не требуется.</span><span class="sxs-lookup"><span data-stu-id="519c8-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="519c8-117">Однако можно использовать модуль «Управление транспортировкой» для определения ставок транспортировки и соответствующей корректировки цены продажи.</span><span class="sxs-lookup"><span data-stu-id="519c8-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="519c8-118">Услуга логистики предоставляется другим юридическим лицом в этой же компании.</span><span class="sxs-lookup"><span data-stu-id="519c8-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="519c8-119">Можно использовать модуль «Управление транспортировкой», рассматривая другое юридическое лицо как любого другого перевозчика.</span><span class="sxs-lookup"><span data-stu-id="519c8-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="519c8-120">Невозможно автоматизировать хозяйственные проводки между юридическими лицами.</span><span class="sxs-lookup"><span data-stu-id="519c8-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="519c8-121">Поэтому необходимо обрабатывать эти проводки вручную (например, путем создания заказа на покупку).</span><span class="sxs-lookup"><span data-stu-id="519c8-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="519c8-122">В юридическом лице, которое предоставляет услуги материально-технического снабжения, модуль «Управление транспортировкой» может использоваться для определения ставок транспортировки.</span><span class="sxs-lookup"><span data-stu-id="519c8-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="519c8-123">Планирование транспортировки в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="519c8-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="519c8-124">В модуле «Управление транспортировкой» планирование транспортировки может быть основано либо на заказах, либо на отгрузках, которые создаются на основе этих заказов.</span><span class="sxs-lookup"><span data-stu-id="519c8-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="519c8-125">Отгрузки всегда существуют в некоторый момент времени, но они не являются необходимыми для планирования транспортировки.</span><span class="sxs-lookup"><span data-stu-id="519c8-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="519c8-126">Заказы на перемещение являются частью исходящего сценария и могут планироваться вместе с заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="519c8-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Рисунок погрузки](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="519c8-128">Входящая транспортировка</span><span class="sxs-lookup"><span data-stu-id="519c8-128">Inbound transportation</span></span>
<span data-ttu-id="519c8-129">Если при заказе номенклатур у поставщика номенклатуры должны быть доставлены на ваш склад, может потребоваться организовать транспортировку номенклатур самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="519c8-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="519c8-130">Можно использовать Finance and Operations для планирования транспортировки и оформления прихода входящей загрузки.</span><span class="sxs-lookup"><span data-stu-id="519c8-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="519c8-131">На следующем рисунке показан бизнес-процесс планирования транспортировки входящей загрузки.</span><span class="sxs-lookup"><span data-stu-id="519c8-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Схема бизнес-процесса для транспортировки входящих загрузок](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="519c8-133">Исходящая транспортировка</span><span class="sxs-lookup"><span data-stu-id="519c8-133">Outbound transportation</span></span>
<span data-ttu-id="519c8-134">Можно планировать и обрабатывать исходящую загрузку для отгрузки определенных номенклатур со склада компании клиенту.</span><span class="sxs-lookup"><span data-stu-id="519c8-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="519c8-135">Можно использовать Finance and Operations для планирования транспортировки и отгрузки исходящей загрузки.</span><span class="sxs-lookup"><span data-stu-id="519c8-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="519c8-136">На следующем рисунке показан бизнес-процесс планирования и обработки исходящих загрузок для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="519c8-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Планирование и обработка исходящих загрузок](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="519c8-138">Формирование загрузок</span><span class="sxs-lookup"><span data-stu-id="519c8-138">Load building</span></span>
<span data-ttu-id="519c8-139">Finance and Operations предоставляет стратегию построения загрузки, которая называется стратегией построения загрузки на основе объема.</span><span class="sxs-lookup"><span data-stu-id="519c8-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="519c8-140">Эта стратегия позволяет использовать максимальные значения, определенные для высоты и веса в шаблоне загрузки, или переопределить параметры путем ввода новых значений.</span><span class="sxs-lookup"><span data-stu-id="519c8-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="519c8-141">Для использования этой стратегии выберите ее в поле **Стратегия формирования загрузок** на экспресс-вкладке **Настройка** на странице **Рабочее место формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="519c8-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="519c8-142">Кроме того, можно добавить собственные стратегии формирования загрузок, создав новый класс в репозитории прикладных объектов (AOT).</span><span class="sxs-lookup"><span data-stu-id="519c8-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>



