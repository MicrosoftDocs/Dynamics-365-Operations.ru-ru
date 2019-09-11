---
title: Обзор разработки и создания соглашений о сервисном обслуживании
description: В соглашении на сервисное обслуживание можно определить ресурсы, использованные в ходе стандартного визита с целью обслуживания, и как оформить накладную на эти ресурсы для клиента.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae7c3b6e1df9751d886f6eeff778e8045bd7df85
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865953"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="9adb1-103">Обзор разработки и создания соглашений о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="9adb1-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9adb1-104">В соглашении на сервисное обслуживание можно определить ресурсы, использованные в ходе стандартного визита с целью обслуживания, и как оформить накладную на эти ресурсы для клиента.</span><span class="sxs-lookup"><span data-stu-id="9adb1-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="9adb1-105">Все соглашения на сервисное обслуживание присоединяются к проектам, на основании которых осуществляется разноска проводок и оформление накладных.</span><span class="sxs-lookup"><span data-stu-id="9adb1-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="9adb1-106">Однако вы можете также оформлять накладную по проводкам заказа на обслуживание непосредственно в проекте, без предварительного соединения заказа на обслуживание с соглашением на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="9adb1-107">Такой вариант может оказаться удобным, если заказ на обслуживание предусматривает однократный визит, и скорость оформления проводки превалирует над необходимостью вести подробный учет по клиенту в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="9adb1-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="9adb1-108">Соглашение на обслуживание</span><span class="sxs-lookup"><span data-stu-id="9adb1-108">Service agreement</span></span>

<span data-ttu-id="9adb1-109">В каждом соглашении на обслуживание необходимо указывать проект, код и группу соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="9adb1-110">Группу соглашения на сервисное обслуживание можно использовать для сортировки и организации соглашений на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="9adb1-111">Заголовок соглашения на сервисное обслуживание содержит настройки, которые распространяются на все присоединенный строки соглашения:</span><span class="sxs-lookup"><span data-stu-id="9adb1-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="9adb1-112">Приостановлено или нет соглашение на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="9adb1-113">Если соглашение приостановлено, на его основании невозможно создать заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="9adb1-114">Срок действия соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="9adb1-115">Как будут вставляться строки в заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="9adb1-116">Является ли соглашение на обслуживание шаблоном.</span><span class="sxs-lookup"><span data-stu-id="9adb1-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="9adb1-117">В заголовке соглашения на сервисное обслуживание можно также настроить все Объекты сервисного обслуживания и Задачи сервисного обслуживания, которые могут использоваться с соглашением на сервисное обслуживание, введя конкретные задачи и объекты сервисного обслуживания, которые необходимо присоединить к различным строкам соглашения.</span><span class="sxs-lookup"><span data-stu-id="9adb1-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="9adb1-118">Из заголовка соглашения на сервисное обслуживание можно также копировать строки соглашения или строки шаблона в текущее соглашение на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="9adb1-119">Имеется возможность приостанавливать соглашения на обслуживание целиком или останавливать отдельные его строки.</span><span class="sxs-lookup"><span data-stu-id="9adb1-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="9adb1-120">Если на строке соглашения на обслуживание установить флажок **Приостановлено**, будет невозможно следующее:</span><span class="sxs-lookup"><span data-stu-id="9adb1-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="9adb1-121">Автоматическое создание и создание вручную заказов на обслуживание из данного соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="9adb1-122">Если на строке соглашения на обслуживание установить флажок **Остановлено**, будет невозможно следующее:</span><span class="sxs-lookup"><span data-stu-id="9adb1-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="9adb1-123">Автоматическое создание и создание вручную заказов на обслуживание из строки соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="9adb1-124">Копирование строки соглашения на обслуживание в другое соглашение или заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="9adb1-125">Если соглашение на сервисное обслуживание приостановлено, остановлены все присоединенные строки независимо от их индивидуального статуса.</span><span class="sxs-lookup"><span data-stu-id="9adb1-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="9adb1-126">Строки соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="9adb1-126">Service-agreement lines</span></span>

<span data-ttu-id="9adb1-127">Каждая строка соглашения на сервисное обслуживание подробно описывает содержание предложенных сервисных работ.</span><span class="sxs-lookup"><span data-stu-id="9adb1-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="9adb1-128">Строки содержат следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="9adb1-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="9adb1-129">Тип проводки и описание типа проводки.</span><span class="sxs-lookup"><span data-stu-id="9adb1-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="9adb1-130">Сотрудник, выполняющий обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="9adb1-131">Объекты, обслуживание которых предусмотрено соглашением на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="9adb1-132">Регистрируются периодичность выполнения работ и связанные проводки номенклатур, расходов и сборов.</span><span class="sxs-lookup"><span data-stu-id="9adb1-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="9adb1-133">Период времени, в течение которого строки заказа на обслуживание можно группировать в заказе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9adb1-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="9adb1-134">Задачи сервисного обслуживания, используемые для группирования наборов строк соглашения в рабочие задачи и для общего описания техникам и клиентам задач сервисного обслуживания, которые будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="9adb1-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="9adb1-135">Прекращено ли действие строки.</span><span class="sxs-lookup"><span data-stu-id="9adb1-135">Whether a line is stopped.</span></span> <span data-ttu-id="9adb1-136">Если выполнение по строке остановлено, вы не сможете создавать заказы на обслуживание для данной строки.</span><span class="sxs-lookup"><span data-stu-id="9adb1-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="9adb1-137">Настройки проекта, такие как категория и свойства строки.</span><span class="sxs-lookup"><span data-stu-id="9adb1-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9adb1-138">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="9adb1-138">Related topics</span></span>

[<span data-ttu-id="9adb1-139">Создание соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="9adb1-139">Create service agreements</span></span>](create-service-agreements.md)
