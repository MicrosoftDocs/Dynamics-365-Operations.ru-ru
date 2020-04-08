---
title: Интегрированные сайты и склады
description: Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173070"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="ebeb7-103">Интегрированные объекты и склады</span><span class="sxs-lookup"><span data-stu-id="ebeb7-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ebeb7-104">Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="ebeb7-105">Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="ebeb7-106">Они используются для моделирования цепочки поставок компании.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="ebeb7-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="ebeb7-107">Templates</span></span>

<span data-ttu-id="ebeb7-108">При интеграции с Common Data Service эти концепции и все связанные с ними сведения доступны в Common Data Service с использованием информационных объектов сайтов и складов в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="ebeb7-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ebeb7-109">Finance and Operations apps</span></span> | <span data-ttu-id="ebeb7-110">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ebeb7-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ebeb7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ebeb7-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="ebeb7-112">Сайты</span><span class="sxs-lookup"><span data-stu-id="ebeb7-112">Sites</span></span> | <span data-ttu-id="ebeb7-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="ebeb7-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="ebeb7-114">Склады</span><span class="sxs-lookup"><span data-stu-id="ebeb7-114">Warehouses</span></span> | <span data-ttu-id="ebeb7-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="ebeb7-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

