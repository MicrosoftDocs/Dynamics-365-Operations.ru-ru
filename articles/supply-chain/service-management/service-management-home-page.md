---
title: "Управление сервисным обслуживанием"
description: "Модуль «Управление обслуживанием» используется для заключения соглашений о сервисном обслуживании и подписок на сервисное обслуживание, обработки заказов на сервисное обслуживание и клиентских запросов, а также для управления оказанием услуг клиентам и анализа оказания услуг клиентам."
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 80a3cb74279f72e8cb94f3a2c38230f409067a47
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.contentlocale: ru-ru
ms.lasthandoff: 05/24/2018

---


# <a name="service-management"></a><span data-ttu-id="f90b5-103">Управление сервисным обслуживанием</span><span class="sxs-lookup"><span data-stu-id="f90b5-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f90b5-104">Модуль **Управление сервисным обслуживанием** используется для заключения соглашений о сервисном обслуживании и подписок на сервисное обслуживание, обработки заказов на сервисное обслуживание и клиентских запросов, а также для управления оказанием услуг клиентам и анализа оказания услуг клиентам.</span><span class="sxs-lookup"><span data-stu-id="f90b5-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="f90b5-105">Соглашения о сервисном обслуживании можно использовать для определения ресурсов, используемых в типовом сервисном визите.</span><span class="sxs-lookup"><span data-stu-id="f90b5-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="f90b5-106">Также можно использовать соглашения о сервисном обслуживании для просмотра того, как по этим ресурсам выставляются накладные клиенту.</span><span class="sxs-lookup"><span data-stu-id="f90b5-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="f90b5-107">Соглашение о сервисном обслуживании может также включать в себя соглашение об условиях обслуживания, которое определяет стандартное время реакции и предусматривает инструменты для записи фактического времени.</span><span class="sxs-lookup"><span data-stu-id="f90b5-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="f90b5-108">Можно создавать заказы на сервисное обслуживание для управления сведениями о запланированных и незапланированных визитах сервисного специалиста на объект клиента.</span><span class="sxs-lookup"><span data-stu-id="f90b5-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="f90b5-109">В заказы на сервисное обслуживание включаются такие сведения, как:</span><span class="sxs-lookup"><span data-stu-id="f90b5-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="f90b5-110">Часы работы сервисного специалиста</span><span class="sxs-lookup"><span data-stu-id="f90b5-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="f90b5-111">Тип услуги или ремонта</span><span class="sxs-lookup"><span data-stu-id="f90b5-111">The type of service or repair</span></span>

3.  <span data-ttu-id="f90b5-112">Ремонтируемая номенклатура, включая сведения о симптомах и диагнозе</span><span class="sxs-lookup"><span data-stu-id="f90b5-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="f90b5-113">Все расходы и сборы, относящиеся к обслуживанию или ремонту</span><span class="sxs-lookup"><span data-stu-id="f90b5-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="f90b5-114">Запросы на сервисное обслуживание можно получать, обрабатывать и исполнять.</span><span class="sxs-lookup"><span data-stu-id="f90b5-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="f90b5-115">После создания заказа на сервисное обслуживание можно использовать этапы сервисного обслуживания для отслеживания хода выполнения и задания правил, определяющих действия, включаемые на каждом этапе.</span><span class="sxs-lookup"><span data-stu-id="f90b5-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="f90b5-116">Когда заказ на сервисное обслуживание выполнен, можно подписать заказ, чтобы подтвердить его выполнение, а затем разнести заказ, чтобы запустить процесс выставления накладной.</span><span class="sxs-lookup"><span data-stu-id="f90b5-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="f90b5-117">Средства отчетности можно использовать для мониторинга резервов заказов на сервисное обслуживание и транзакциям по подпискам, а также печатать описания работ и приходы работ.</span><span class="sxs-lookup"><span data-stu-id="f90b5-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="f90b5-118">Бизнес-процессы</span><span class="sxs-lookup"><span data-stu-id="f90b5-118">Business processes</span></span>

<span data-ttu-id="f90b5-119">Следующая схема иллюстрирует высокоуровневые бизнес-процессы для модуля **Управление сервисным обслуживанием** и точки интеграции процессов сервисного обслуживания с другими модулями в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f90b5-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f90b5-120">[![Диаграмма бизнес-процесса управления услугами](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="f90b5-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="f90b5-121">Обзор модуля "Управление сервисным обслуживанием"</span><span class="sxs-lookup"><span data-stu-id="f90b5-121">Service management at a glance</span></span>

|<span data-ttu-id="f90b5-122">Важные задачи</span><span class="sxs-lookup"><span data-stu-id="f90b5-122">Important tasks</span></span>           | <span data-ttu-id="f90b5-123">Первичные страницы</span><span class="sxs-lookup"><span data-stu-id="f90b5-123">Primary pages</span></span>                         |<span data-ttu-id="f90b5-124">Популярные отчеты</span><span class="sxs-lookup"><span data-stu-id="f90b5-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="f90b5-125">Выполнение соглашений о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="f90b5-125">Fulfill service agreements</span></span>|<span data-ttu-id="f90b5-126">Соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="f90b5-126">Service agreements</span></span>                     |<span data-ttu-id="f90b5-127">Резерв заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="f90b5-127">Service order margin</span></span>         |
|<span data-ttu-id="f90b5-128">Обработка запросов клиентов</span><span class="sxs-lookup"><span data-stu-id="f90b5-128">Handle customer inquiries</span></span> |<span data-ttu-id="f90b5-129">Заказы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="f90b5-129">Service orders</span></span>                         |<span data-ttu-id="f90b5-130">Описание работы</span><span class="sxs-lookup"><span data-stu-id="f90b5-130">Work description</span></span>             |
|                          |<span data-ttu-id="f90b5-131">Панель подготовки к отправке</span><span class="sxs-lookup"><span data-stu-id="f90b5-131">Dispatch board</span></span>                         |<span data-ttu-id="f90b5-132">Проводка - Подписка</span><span class="sxs-lookup"><span data-stu-id="f90b5-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="f90b5-133">транзакции по сборам по подписке</span><span class="sxs-lookup"><span data-stu-id="f90b5-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="f90b5-134">Интеграция модуля "Управление сервисным обслуживанием"</span><span class="sxs-lookup"><span data-stu-id="f90b5-134">Integration of Service management</span></span>

<span data-ttu-id="f90b5-135">Управление сервисным обслуживанием может интегрироваться со следующими модулями:</span><span class="sxs-lookup"><span data-stu-id="f90b5-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="f90b5-136">Продажи и маркетинг</span><span class="sxs-lookup"><span data-stu-id="f90b5-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="f90b5-137">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="f90b5-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


