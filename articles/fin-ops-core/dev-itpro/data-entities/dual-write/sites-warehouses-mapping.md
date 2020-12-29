---
title: Интегрированные сайты и склады
description: Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679328"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="d1d70-103">Интегрированные объекты и склады</span><span class="sxs-lookup"><span data-stu-id="d1d70-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="d1d70-104">Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d1d70-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="d1d70-105">Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d1d70-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="d1d70-106">Они используются для моделирования цепочки поставок компании.</span><span class="sxs-lookup"><span data-stu-id="d1d70-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="d1d70-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d1d70-107">Templates</span></span>

<span data-ttu-id="d1d70-108">При интеграции с Dataverse эти концепции и все связанные с ними сведения доступны в Dataverse с использованием информационных таблиц сайтов и складов в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d1d70-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="d1d70-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1d70-109">Finance and Operations apps</span></span> | <span data-ttu-id="d1d70-110">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d1d70-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d1d70-111">описание</span><span class="sxs-lookup"><span data-stu-id="d1d70-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="d1d70-112">Сайты</span><span class="sxs-lookup"><span data-stu-id="d1d70-112">Sites</span></span> | <span data-ttu-id="d1d70-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="d1d70-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="d1d70-114">Склады</span><span class="sxs-lookup"><span data-stu-id="d1d70-114">Warehouses</span></span> | <span data-ttu-id="d1d70-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="d1d70-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

