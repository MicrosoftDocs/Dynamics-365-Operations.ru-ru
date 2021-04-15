---
title: Интегрированные сайты и склады
description: Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750674"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="c6a76-103">Интегрированные объекты и склады</span><span class="sxs-lookup"><span data-stu-id="c6a76-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="c6a76-104">Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c6a76-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="c6a76-105">Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c6a76-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="c6a76-106">Они используются для моделирования цепочки поставок компании.</span><span class="sxs-lookup"><span data-stu-id="c6a76-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="c6a76-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c6a76-107">Templates</span></span>

<span data-ttu-id="c6a76-108">При интеграции с Dataverse эти концепции и все связанные с ними сведения доступны в Dataverse с использованием информационных таблиц сайтов и складов в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c6a76-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="c6a76-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6a76-109">Finance and Operations apps</span></span> | <span data-ttu-id="c6a76-110">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c6a76-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="c6a76-111">описание</span><span class="sxs-lookup"><span data-stu-id="c6a76-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="c6a76-112">Сайты</span><span class="sxs-lookup"><span data-stu-id="c6a76-112">Sites</span></span> | <span data-ttu-id="c6a76-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="c6a76-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="c6a76-114">Склады</span><span class="sxs-lookup"><span data-stu-id="c6a76-114">Warehouses</span></span> | <span data-ttu-id="c6a76-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="c6a76-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]