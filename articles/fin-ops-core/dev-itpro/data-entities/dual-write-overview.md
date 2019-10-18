---
title: Интеграция данных между Finance and Operations и Common Data Service почти в режиме реального времени
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
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184493"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="e4e8e-103">Интеграция данных почти в реальном времени с Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e4e8e-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="e4e8e-104">В современном цифровом мире бизнес-экосистемы используют приложения Microsoft Dynamics 365 как единое целое.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="e4e8e-105">Поскольку данные от людей, клиентов, операций и устройств Интернета вещей (IoT) стекаются в один источник, есть возможность для цифровых циклов обратной связи.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="e4e8e-106">Для достижения этого опыта важна интеграция между приложениями Finance and Operations и другими приложениями Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="e4e8e-107">Некоторые приложения строятся на основе Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="e4e8e-108">Интеграция данных между приложениями Finance and Operations с Common Data Service позволяет другим приложениям взаимодействовать согласованно и свободно с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="e4e8e-109">Приложения Finance and Operations и Common Data Service обеспечивают синхронизацию данных почти в режиме реального времени между приложениями Finance and Operations и другими приложениями Dynamics 365 через систему двойной записи.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="e4e8e-110">Охват широк и включает 28 поверхностных областей приложения.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="e4e8e-111">Цель состоит в том, чтобы обеспечить пользовательский опыт "одного Dynamics 365" через бесшовные потоки данных, которые соединяют бизнес-процессы между приложениями.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Диаграмма обзора архитектуры](media/dual-write-overview.jpg)

<span data-ttu-id="e4e8e-113">Следующие ценностные предложения доступны для клиентов:</span><span class="sxs-lookup"><span data-stu-id="e4e8e-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="e4e8e-114">Организационная иерархия в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e4e8e-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="e4e8e-115">Концепция компании в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e4e8e-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="e4e8e-116">Интегрированный мастер клиентов</span><span class="sxs-lookup"><span data-stu-id="e4e8e-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="e4e8e-117">Интегрированный мастер поставщиков</span><span class="sxs-lookup"><span data-stu-id="e4e8e-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="e4e8e-118">Единый шаблон продукта</span><span class="sxs-lookup"><span data-stu-id="e4e8e-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="e4e8e-119">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="e4e8e-119">System requirements</span></span>

<span data-ttu-id="e4e8e-120">Синхронные, двунаправленные, практически в режиме реального времени потоки данных требуют следующих версий:</span><span class="sxs-lookup"><span data-stu-id="e4e8e-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="e4e8e-121">Microsoft Dynamics 365 for Finance and Operations версии 10.0.4 (июль 2019 г.) с обновлением платформы Platform update 28 или выше</span><span class="sxs-lookup"><span data-stu-id="e4e8e-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="e4e8e-122">Microsoft Dynamics 365 for Customer Engagement, платформа версии 9.1 (4.2) или более новая версия</span><span class="sxs-lookup"><span data-stu-id="e4e8e-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="e4e8e-123">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="e4e8e-123">Setup instructions</span></span>

<span data-ttu-id="e4e8e-124">Выполните следующие шаги, чтобы настроить интеграцию между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="e4e8e-125">Для настройки системы двойной записи, см. [пошаговое руководство](https://aka.ms/dualwrite-docs) в объявлении предварительной версии двойной записи.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="e4e8e-126">Скачайте и установите решение из группы [Интеграция Finance and Operations, Common Data Service и Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) в Yammer.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="e4e8e-127">Пакет содержит пять решений:</span><span class="sxs-lookup"><span data-stu-id="e4e8e-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="e4e8e-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="e4e8e-128">Dynamics365Company</span></span>
    + <span data-ttu-id="e4e8e-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="e4e8e-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="e4e8e-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="e4e8e-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="e4e8e-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="e4e8e-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="e4e8e-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="e4e8e-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="e4e8e-133">Следуйте порядку выполнения для [синхронизации исходных справочных данных](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="e4e8e-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="e4e8e-134">Если вы столкнулись с проблемами синхронизации с двойной записью, см. [Руководство по устранению неполадок для интеграции данных](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="e4e8e-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4e8e-135">Вы не можете запустить двойную запись и [продажу перспективному клиенту](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) бок о бок.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="e4e8e-136">Если вы выполняете решение "Продажа перспективному клиенту", вы должны удалить его.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="e4e8e-137">Вы также должны отключить шаблоны двойной записи для клиентов и поставщиков, которые являются частью решения продажи перспективному клиенту.</span><span class="sxs-lookup"><span data-stu-id="e4e8e-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
