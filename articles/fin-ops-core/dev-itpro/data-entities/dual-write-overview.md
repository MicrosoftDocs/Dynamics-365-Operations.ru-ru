---
title: Интеграция данных почти в реальном времени с Common Data Service
description: Эта тема содержит обзор интеграции между Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853914"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="65165-103">Интеграция данных почти в реальном времени с Common Data Service</span><span class="sxs-lookup"><span data-stu-id="65165-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65165-104">В современном цифровом мире бизнес-экосистемы используют приложения Microsoft Dynamics 365 как единое целое.</span><span class="sxs-lookup"><span data-stu-id="65165-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="65165-105">Поскольку данные от людей, клиентов, операций и устройств Интернета вещей (IoT) стекаются в один источник, есть возможность для цифровых циклов обратной связи.</span><span class="sxs-lookup"><span data-stu-id="65165-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="65165-106">Для достижения этого опыта важна интеграция между приложениями Finance and Operations и другими приложениями Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="65165-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="65165-107">Некоторые приложения строятся на основе Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="65165-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="65165-108">Интеграция данных между приложениями Finance and Operations с Common Data Service позволяет другим приложениям взаимодействовать согласованно и свободно с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="65165-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="65165-109">Приложения Finance and Operations и Common Data Service обеспечивают синхронизацию данных почти в режиме реального времени между приложениями Finance and Operations и другими приложениями Dynamics 365 через систему двойной записи.</span><span class="sxs-lookup"><span data-stu-id="65165-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="65165-110">Охват широк и включает 28 поверхностных областей приложения.</span><span class="sxs-lookup"><span data-stu-id="65165-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="65165-111">Цель состоит в том, чтобы обеспечить пользовательский опыт "одного Dynamics 365" через бесшовные потоки данных, которые соединяют бизнес-процессы между приложениями.</span><span class="sxs-lookup"><span data-stu-id="65165-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Диаграмма обзора архитектуры](media/dual-write-overview.jpg)

<span data-ttu-id="65165-113">Следующие ценностные предложения доступны:</span><span class="sxs-lookup"><span data-stu-id="65165-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="65165-114">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="65165-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="65165-115">Концепция компании в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="65165-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="65165-116">Интегрированный мастер клиентов</span><span class="sxs-lookup"><span data-stu-id="65165-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="65165-117">Интегрированная ГК</span><span class="sxs-lookup"><span data-stu-id="65165-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="65165-118">Унифицированный опыт работы с продуктом</span><span class="sxs-lookup"><span data-stu-id="65165-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="65165-119">Интегрированный мастер поставщиков</span><span class="sxs-lookup"><span data-stu-id="65165-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="65165-120">Интегрированные сайты и склады</span><span class="sxs-lookup"><span data-stu-id="65165-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="65165-121">Интегрированная налоговый справочник</span><span class="sxs-lookup"><span data-stu-id="65165-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="65165-122">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="65165-122">System requirements</span></span>

<span data-ttu-id="65165-123">Синхронные, двунаправленные, практически в режиме реального времени потоки данных требуют следующих версий:</span><span class="sxs-lookup"><span data-stu-id="65165-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="65165-124">Microsoft Dynamics 365 for Finance and Operations версии 10.0.4 (июль 2019 г.) с обновлением платформы Platform update 28 или выше</span><span class="sxs-lookup"><span data-stu-id="65165-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="65165-125">Microsoft Dynamics 365 for Customer Engagement, платформа версии 9.1 (4.2) или более новая версия</span><span class="sxs-lookup"><span data-stu-id="65165-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="65165-126">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="65165-126">Setup instructions</span></span>

<span data-ttu-id="65165-127">Выполните следующие шаги, чтобы настроить интеграцию между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="65165-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="65165-128">Для настройки системы двойной записи, см. [пошаговое руководство](https://aka.ms/dualwrite-docs) в объявлении предварительной версии двойной записи.</span><span class="sxs-lookup"><span data-stu-id="65165-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="65165-129">Загрузите и установите решение из группы Yammer [Fin Ops и CDS/CE Integration через Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096).</span><span class="sxs-lookup"><span data-stu-id="65165-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="65165-130">Пакет содержит пять решений:</span><span class="sxs-lookup"><span data-stu-id="65165-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="65165-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="65165-131">Dynamics365Company</span></span>
    + <span data-ttu-id="65165-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="65165-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="65165-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="65165-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="65165-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="65165-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="65165-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="65165-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="65165-136">Следуйте порядку выполнения для [синхронизации исходных справочных данных](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="65165-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="65165-137">Если вы столкнулись с проблемами синхронизации с двойной записью, см. [Руководство по устранению неполадок для интеграции данных](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="65165-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65165-138">Вы не можете запустить двойную запись и [продажу перспективному клиенту](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) бок о бок.</span><span class="sxs-lookup"><span data-stu-id="65165-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="65165-139">Если вы выполняете решение "Продажа перспективному клиенту", вы должны удалить его.</span><span class="sxs-lookup"><span data-stu-id="65165-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="65165-140">Вы также должны отключить шаблоны двойной записи для клиентов и поставщиков, которые являются частью решения продажи перспективному клиенту.</span><span class="sxs-lookup"><span data-stu-id="65165-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
