---
title: Внутренние активы для обслуживания
description: В этом разделе описывается, как можно использовать Microsoft Dynamics 365 Field Service для обслуживания как клиентских активов, так и внутренних активов.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748601"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="d9c61-103">Внутренние активы для обслуживания</span><span class="sxs-lookup"><span data-stu-id="d9c61-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d9c61-104">Microsoft Dynamics 365 Field Service разработано для обслуживания активов клиентов.</span><span class="sxs-lookup"><span data-stu-id="d9c61-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="d9c61-105">Управление активами для Dynamics 365 Supply Chain Management предназначено для ведения внутренних активов.</span><span class="sxs-lookup"><span data-stu-id="d9c61-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="d9c61-106">Интеграция этих двух приложений позволяет использовать Field Service для обслуживания как активов клиентов, так и внутренних активов.</span><span class="sxs-lookup"><span data-stu-id="d9c61-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="d9c61-107">Имеется также возможность классифицировать активы на основе функционального местоположения или иерархии и отслеживать обслуживание на подробном уровне.</span><span class="sxs-lookup"><span data-stu-id="d9c61-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="d9c61-108">Дополнительные сведения см. в разделе [Интеграция Dynamics 365 Field Service и Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="d9c61-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="d9c61-109">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d9c61-109">Templates</span></span>

<span data-ttu-id="d9c61-110">Внутренние активы включают коллекцию сопоставлений основных таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d9c61-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="d9c61-111">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d9c61-111">Finance and Operations apps</span></span> | <span data-ttu-id="d9c61-112">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d9c61-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="d9c61-113">описание</span><span class="sxs-lookup"><span data-stu-id="d9c61-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="d9c61-114">Модели жизненного цикла актива в управлении активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="d9c61-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d9c61-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="d9c61-116">Состояния жизненного цикла актива в управлении активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="d9c61-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d9c61-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="d9c61-118">Активы управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-118">Asset management assets</span></span> | <span data-ttu-id="d9c61-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="d9c61-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="d9c61-120">Типы активов управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-120">Asset management asset types</span></span> | <span data-ttu-id="d9c61-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="d9c61-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="d9c61-122">Модели жизненного цикла функционального местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="d9c61-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d9c61-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="d9c61-124">Состояния жизненного цикла функционального местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="d9c61-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d9c61-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="d9c61-126">Функциональные местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-126">Asset management functional locations</span></span> | <span data-ttu-id="d9c61-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="d9c61-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="d9c61-128">Типы функциональных местоположений управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-128">Asset management functional location types</span></span> | <span data-ttu-id="d9c61-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="d9c61-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="d9c61-130">Производители управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-130">Asset management manufacturers</span></span> | <span data-ttu-id="d9c61-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="d9c61-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="d9c61-132">Модели управление активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-132">Asset management models</span></span> | <span data-ttu-id="d9c61-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="d9c61-133">msdyn\_models</span></span> | |
| <span data-ttu-id="d9c61-134">Гарантия управления активами</span><span class="sxs-lookup"><span data-stu-id="d9c61-134">Asset management warranty</span></span> | <span data-ttu-id="d9c61-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="d9c61-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]