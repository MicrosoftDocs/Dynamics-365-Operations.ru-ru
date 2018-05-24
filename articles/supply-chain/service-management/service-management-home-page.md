---
title: "Управление сервисным обслуживанием"
description: "Модуль «Управление обслуживанием» используется для заключения соглашений о сервисном обслуживании и подписок на сервисное обслуживание, обработки заказов на сервисное обслуживание и клиентских запросов, а также для управления оказанием услуг клиентам и анализа оказания услуг клиентам."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: ru-ru
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="463d8-103">Управление сервисным обслуживанием</span><span class="sxs-lookup"><span data-stu-id="463d8-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="463d8-104">Модуль **Управление сервисным обслуживанием** используется для заключения соглашений о сервисном обслуживании и подписок на сервисное обслуживание, обработки заказов на сервисное обслуживание и клиентских запросов, а также для управления оказанием услуг клиентам и анализа оказания услуг клиентам.</span><span class="sxs-lookup"><span data-stu-id="463d8-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="463d8-105">Соглашения о сервисном обслуживании можно использовать для определения ресурсов, используемых в типовом сервисном визите.</span><span class="sxs-lookup"><span data-stu-id="463d8-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="463d8-106">Также можно использовать соглашения о сервисном обслуживании для просмотра того, как по этим ресурсам выставляются накладные клиенту.</span><span class="sxs-lookup"><span data-stu-id="463d8-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="463d8-107">Соглашение о сервисном обслуживании может также включать в себя соглашение об условиях обслуживания, которое определяет стандартное время реакции и предусматривает инструменты для записи фактического времени.</span><span class="sxs-lookup"><span data-stu-id="463d8-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="463d8-108">Можно создавать заказы на сервисное обслуживание для управления сведениями о запланированных и незапланированных визитах сервисного специалиста на объект клиента.</span><span class="sxs-lookup"><span data-stu-id="463d8-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="463d8-109">В заказы на сервисное обслуживание включаются такие сведения, как:</span><span class="sxs-lookup"><span data-stu-id="463d8-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="463d8-110">Часы работы сервисного специалиста</span><span class="sxs-lookup"><span data-stu-id="463d8-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="463d8-111">Тип услуги или ремонта</span><span class="sxs-lookup"><span data-stu-id="463d8-111">The type of service or repair</span></span>

3.  <span data-ttu-id="463d8-112">Ремонтируемая номенклатура, включая сведения о симптомах и диагнозе</span><span class="sxs-lookup"><span data-stu-id="463d8-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="463d8-113">Все расходы и сборы, относящиеся к обслуживанию или ремонту</span><span class="sxs-lookup"><span data-stu-id="463d8-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="463d8-114">Клиенты могут подавать запросы на сервисное обслуживание через Интернет с помощью корпоративного портала.</span><span class="sxs-lookup"><span data-stu-id="463d8-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="463d8-115">Эти запросы можно получать, обрабатывать и исполнять.</span><span class="sxs-lookup"><span data-stu-id="463d8-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="463d8-116">После создания заказа на сервисное обслуживание можно использовать этапы сервисного обслуживания для отслеживания хода выполнения и задания правил, определяющих действия, включаемые на каждом этапе.</span><span class="sxs-lookup"><span data-stu-id="463d8-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="463d8-117">Когда заказ на сервисное обслуживание выполнен, можно подписать заказ, чтобы подтвердить его выполнение, а затем разнести заказ, чтобы запустить процесс выставления накладной.</span><span class="sxs-lookup"><span data-stu-id="463d8-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="463d8-118">Средства отчетности можно использовать для мониторинга резервов заказов на сервисное обслуживание и проводкам по подпискам, а также печатать описания работ и приходы работ.</span><span class="sxs-lookup"><span data-stu-id="463d8-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="463d8-119">Бизнес-процессы</span><span class="sxs-lookup"><span data-stu-id="463d8-119">Business processes</span></span>

<span data-ttu-id="463d8-120">Следующая схема иллюстрирует высокоуровневые бизнес-процессы для модуля **Управление сервисным обслуживанием** и точки интеграции процессов сервисного обслуживания с другими модулями в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="463d8-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="463d8-121">[![Диаграмма бизнес-процесса управления услугами](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="463d8-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="463d8-122">Обзор модуля "Управление сервисным обслуживанием"</span><span class="sxs-lookup"><span data-stu-id="463d8-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="463d8-123">Важные задачи</span><span class="sxs-lookup"><span data-stu-id="463d8-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="463d8-124">Основные формы</span><span class="sxs-lookup"><span data-stu-id="463d8-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="463d8-125">Популярные отчеты</span><span class="sxs-lookup"><span data-stu-id="463d8-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="463d8-126">Выполнение соглашений на обслуживание</span><span class="sxs-lookup"><span data-stu-id="463d8-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="463d8-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Соглашения на обслуживании (форма)</a></span><span class="sxs-lookup"><span data-stu-id="463d8-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="463d8-128"><strong>Резерв заказа на обслуживание</strong></span><span class="sxs-lookup"><span data-stu-id="463d8-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="463d8-129">Обработка запросов клиентов</span><span class="sxs-lookup"><span data-stu-id="463d8-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="463d8-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Заказы на обслуживание (форма)</a></span><span class="sxs-lookup"><span data-stu-id="463d8-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="463d8-131"><strong>Описание работы</strong></span><span class="sxs-lookup"><span data-stu-id="463d8-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="463d8-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Панель подготовки к отправке (форма)</a></span><span class="sxs-lookup"><span data-stu-id="463d8-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="463d8-133"><strong>Проводка - Подписка</strong></span><span class="sxs-lookup"><span data-stu-id="463d8-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="463d8-134"><strong>Проводки по сборам по подписке</strong></span><span class="sxs-lookup"><span data-stu-id="463d8-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="463d8-135">Интеграция модуля "Управление сервисным обслуживанием"</span><span class="sxs-lookup"><span data-stu-id="463d8-135">Integration of Service management</span></span>

<span data-ttu-id="463d8-136">Управление сервисным обслуживанием может интегрироваться со следующими модулями в Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="463d8-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="463d8-137">Продажи и маркетинг</span><span class="sxs-lookup"><span data-stu-id="463d8-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="463d8-138">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="463d8-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


