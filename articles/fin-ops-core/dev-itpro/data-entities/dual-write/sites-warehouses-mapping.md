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
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019975"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="0dcdf-103">Интегрированные объекты и склады</span><span class="sxs-lookup"><span data-stu-id="0dcdf-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0dcdf-104">Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="0dcdf-105">Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="0dcdf-106">Они используются для моделирования цепочки поставок компании.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="0dcdf-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="0dcdf-107">Templates</span></span>

<span data-ttu-id="0dcdf-108">При интеграции с Common Data Service эти концепции и все связанные с ними сведения доступны в Common Data Service с использованием информационных объектов сайтов и складов в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="0dcdf-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0dcdf-109">Finance and Operations apps</span></span> | <span data-ttu-id="0dcdf-110">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0dcdf-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0dcdf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0dcdf-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="0dcdf-112">Сайты</span><span class="sxs-lookup"><span data-stu-id="0dcdf-112">Sites</span></span> | <span data-ttu-id="0dcdf-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="0dcdf-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="0dcdf-114">Склады</span><span class="sxs-lookup"><span data-stu-id="0dcdf-114">Warehouses</span></span> | <span data-ttu-id="0dcdf-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0dcdf-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

