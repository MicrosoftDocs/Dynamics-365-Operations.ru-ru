---
title: "Запуск производственных заказов"
description: "Выпущенный производственный заказ — это заказ, который был утвержден для запуска в производство. Термин \"выпущенный\" используются для описания состояния в жизненном цикле производственного заказа, когда производственный заказ доступен для выполнения в производственном цехе или для процессов склада."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0e7f3747980ff2fb5d055c9496167888e067f8d
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="release-production-orders"></a><span data-ttu-id="4e1a8-104">Запуск производственных заказов</span><span class="sxs-lookup"><span data-stu-id="4e1a8-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e1a8-105">Выпущенный производственный заказ — это заказ, который был утвержден для запуска в производство.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="4e1a8-106">Термин "выпущенный" используются для описания состояния в жизненном цикле производственного заказа, когда производственный заказ доступен для выполнения в производственном цехе или для процессов склада.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="4e1a8-107">Характеристики состояния "Выпущено"</span><span class="sxs-lookup"><span data-stu-id="4e1a8-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="4e1a8-108">Состояние **Выпущено** — это одно из состояний в жизненном цикле производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="4e1a8-109">Производственные заказы, находящиеся в состоянии **Выпущено**, доступны для исполнения на производственном цехе и для процессов склада.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="4e1a8-110">Состояние **Выпущено** имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="4e1a8-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="4e1a8-111">Состояние производственного заказа можно изменить на **Выпущено** либо из производственного заказа, либо с помощью процесса пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="4e1a8-112">Производственный заказ может также обновляться автоматически из запланированных производственных заказов, которые подтверждены с помощью поля **Временная граница** на странице **Сводный план**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="4e1a8-113">Состояние **Выпущено** является сигналом для операторов цеха (операторов) на начало выполнения производственных заданий в цехе.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="4e1a8-114">Производственные бумаги, такие как карты маршрута, маршрутные задания и карты заданий обеспечивают информацию о производственных заданиях и могут быть выпущены.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="4e1a8-115">Для физически зарезервированных материалов создается работа склада, чтобы подобрать материалы для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="4e1a8-116">Выпуск заданий в цеху</span><span class="sxs-lookup"><span data-stu-id="4e1a8-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="4e1a8-117">После выпуска производственного заказа производственные задания, связанные с этим заказом, становятся видны и готовы для регистрации.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="4e1a8-118">Операторы могут регистрировать задания, такие как "Начало", "Остановка" и "Завершение", на странице **Терминал карт заданий** или **Карта задания — устройство**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="4e1a8-119">Зарегистрированные время и количество автоматически переносятся со страниц регистрации в производственные журналы, чтобы отслеживать израсходованные время и количество.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="4e1a8-120">Карты маршрутов</span><span class="sxs-lookup"><span data-stu-id="4e1a8-120">Route cards</span></span>
<span data-ttu-id="4e1a8-121">В карте маршрута содержится общая информация, возникающая при настройке маршрута и операции и выборе способа планирования операций и заданий.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="4e1a8-122">Маршрутные задания</span><span class="sxs-lookup"><span data-stu-id="4e1a8-122">Route jobs</span></span>
<span data-ttu-id="4e1a8-123">В маршрутном задании подробно описывается каждое задание операции, включая время установки, обработки, нахождении в очереди и транспортировки.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="4e1a8-124">Например, такая операция, как окраска, может потребовать отдельных заданий, таких как время настройки, время выполнения (для процесса покраски) и время пребывания в очереди (для сушки).</span><span class="sxs-lookup"><span data-stu-id="4e1a8-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="4e1a8-125">Карты заданий</span><span class="sxs-lookup"><span data-stu-id="4e1a8-125">Job cards</span></span>
<span data-ttu-id="4e1a8-126">Карта задания включает номера отдельных заданий по определенной операции.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="4e1a8-127">Одно задание на каждой странице.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-127">One job appears on each page.</span></span> <span data-ttu-id="4e1a8-128">Задания, включенные в карту заданий, и расчетное время их выполнения определены в данных настройки маршрута и операции.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="4e1a8-129">Из карточки задания вы можете открыть страницу **Строки производственного журнала**, **карта задания**.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="4e1a8-130">Сотрудники, обеспечивающие функционирование ресурсов операции, могут оставлять отзывы по процессу производства.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="4e1a8-131">Предусмотрены поля для ввода статистики потребления и других сведений, например, количества ошибок.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="4e1a8-132">Работа склада для комплектации сырья</span><span class="sxs-lookup"><span data-stu-id="4e1a8-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="4e1a8-133">Работа для комплектации сырья создается во время выпуска.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="4e1a8-134">Работа создается только для количества материалов, которое было физически зарезервировано для производственного заказа до выпуска этого заказа.</span><span class="sxs-lookup"><span data-stu-id="4e1a8-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="4e1a8-135">Следующая настройка необходима, чтобы создать работу склада для комплектации сырья:</span><span class="sxs-lookup"><span data-stu-id="4e1a8-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="4e1a8-136">Директива положения для комплектации сырья, которая определяет, в каком местоположении склада следует комплектовать материалы</span><span class="sxs-lookup"><span data-stu-id="4e1a8-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="4e1a8-137">Шаблон волны для сырья, где установлены политики для выполнения работы склада</span><span class="sxs-lookup"><span data-stu-id="4e1a8-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="4e1a8-138">Местоположение начала производства, которое определяет, куда помещаются материалы</span><span class="sxs-lookup"><span data-stu-id="4e1a8-138">A production input location that determines where materials are put</span></span>





