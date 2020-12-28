---
title: Обзор модуля управления складом
description: Управление складом используется для отслеживания и автоматизации процессов склада.
author: ShylaThompson
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad0659a86e75dc4a5a204ebc05405f62abf2ca1e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4436417"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="3e012-103">Обзор управления складом</span><span class="sxs-lookup"><span data-stu-id="3e012-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e012-104">Модуль "Управление складом" позволяет управлять процессами склада в производственных компаниях, компаниях-дистрибьюторах и компаниях розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="3e012-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="3e012-105">Этот модуль имеет самые разнообразные функции для поддержки оборудования склада оптимального уровня, в любое время.</span><span class="sxs-lookup"><span data-stu-id="3e012-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="3e012-106">Модуль "Управление складом" полностью интегрирован с другими бизнес-процессами , такими как транспортировка, производство, контроль качества, закупки, перемещение, продажи и возвраты.</span><span class="sxs-lookup"><span data-stu-id="3e012-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="3e012-107">Начало работы</span><span class="sxs-lookup"><span data-stu-id="3e012-107">Get started</span></span>
<span data-ttu-id="3e012-108">Для начала работы с модулем "Управление склада" необходимо выполнить настройку общих параметров склада в соответствии с бизнес-процессами в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="3e012-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of your company.</span></span>

- <span data-ttu-id="3e012-109">Перейдите на страницу **Параметры управления складом**, выбрав **Управление складом** > **Настройка**, чтобы настроить общие параметры склада.</span><span class="sxs-lookup"><span data-stu-id="3e012-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="3e012-110">Необходимо настроить компоненты для входящих и исходящих workflow-процессов склада в соответствии с бизнес-требованиями.</span><span class="sxs-lookup"><span data-stu-id="3e012-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="3e012-111">Самые важные компоненты, которые необходимо настроить, — это шаблоны волн, шаблоны работ, пулы работ и директивы местонахождений.</span><span class="sxs-lookup"><span data-stu-id="3e012-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="3e012-112">Обзор конфигурации склада</span><span class="sxs-lookup"><span data-stu-id="3e012-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="3e012-113">Контроль работы склада с шаблонами работы и директивами для мест хранения</span><span class="sxs-lookup"><span data-stu-id="3e012-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="3e012-114">Настройка мобильных устройств для работы склада</span><span class="sxs-lookup"><span data-stu-id="3e012-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="3e012-115">Настройка директивы местонахождения для размещения заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="3e012-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="3e012-116">Настройка рабочего шаблона для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="3e012-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="3e012-117">Процессы управления складом</span><span class="sxs-lookup"><span data-stu-id="3e012-117">Warehouse management processes</span></span>
- <span data-ttu-id="3e012-118">Интегрированная поддержка документов-источников для заказов на продажу, возвратов, заказов на перемещение, производственных заказов и канбана</span><span class="sxs-lookup"><span data-stu-id="3e012-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="3e012-119">Поддержка гибких входящих и исходящих workflow-процессов материалов на основе запросов</span><span class="sxs-lookup"><span data-stu-id="3e012-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="3e012-120">Полная интеграция с решениями "Производство" и "Транспортировка"</span><span class="sxs-lookup"><span data-stu-id="3e012-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="3e012-121">Полный контроль над лимитами хранения и метриками объема местонахождений</span><span class="sxs-lookup"><span data-stu-id="3e012-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="3e012-122">Управление свойствами запасов по статусу запасов</span><span class="sxs-lookup"><span data-stu-id="3e012-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="3e012-123">Полная поддержка партий и номенклатур с серийными номерами</span><span class="sxs-lookup"><span data-stu-id="3e012-123">Full batch and serial item support</span></span>
- <span data-ttu-id="3e012-124">Различные возможности приемки номенклатуры</span><span class="sxs-lookup"><span data-stu-id="3e012-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="3e012-125">Различные стратегии комплектации</span><span class="sxs-lookup"><span data-stu-id="3e012-125">Multiple picking strategies</span></span>
- <span data-ttu-id="3e012-126">Готовая поддержка следующего поколения сканеров штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="3e012-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="3e012-127">Типы палет/контейнеров для складских процессов</span><span class="sxs-lookup"><span data-stu-id="3e012-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="3e012-128">Расширенные возможности для инвентаризации</span><span class="sxs-lookup"><span data-stu-id="3e012-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="3e012-129">Печать этикеток и маршрутизация этикеток с поддержкой Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="3e012-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="3e012-130">Интеграция бизнес-аналитики в Power BI</span><span class="sxs-lookup"><span data-stu-id="3e012-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="3e012-131">Ручное и автоматическое перемещение запасов</span><span class="sxs-lookup"><span data-stu-id="3e012-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="3e012-132">Полностью интегрированный контроль качества (QMS)</span><span class="sxs-lookup"><span data-stu-id="3e012-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="3e012-133">Полная прослеживаемость обработки материалов работниками</span><span class="sxs-lookup"><span data-stu-id="3e012-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="3e012-134">Обработка исходящих волн</span><span class="sxs-lookup"><span data-stu-id="3e012-134">Outbound wave processing</span></span>
- <span data-ttu-id="3e012-135">Поддержка упаковки вручную и автоматической контейнеризации</span><span class="sxs-lookup"><span data-stu-id="3e012-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="3e012-136">Комплектация по кластеру</span><span class="sxs-lookup"><span data-stu-id="3e012-136">Cluster picking</span></span>
- <span data-ttu-id="3e012-137">Простой кросс-докинг</span><span class="sxs-lookup"><span data-stu-id="3e012-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e012-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3e012-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="3e012-139">Новые возможности и текущие разработки</span><span class="sxs-lookup"><span data-stu-id="3e012-139">What's new and in development</span></span>
<span data-ttu-id="3e012-140">Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](https://roadmap.dynamics.com/), чтобы узнать, какие новые функции уже выпущены, а какие еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="3e012-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="3e012-141">Блоги</span><span class="sxs-lookup"><span data-stu-id="3e012-141">Blogs</span></span>
<span data-ttu-id="3e012-142">Мнения, новости и другие сведения об управлении складом и других решениях см. в [блоге по Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="3e012-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

