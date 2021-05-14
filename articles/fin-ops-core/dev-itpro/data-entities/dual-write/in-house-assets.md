---
title: Внутренние активы для обслуживания
description: В этом разделе описывается, как можно использовать Microsoft Dynamics 365 Field Service для обслуживания как клиентских, так и внутренних активов.
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
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941422"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="d43ae-103">Внутренние активы для обслуживания</span><span class="sxs-lookup"><span data-stu-id="d43ae-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d43ae-104">Microsoft Dynamics 365 Field Service разработано для обслуживания активов клиентов.</span><span class="sxs-lookup"><span data-stu-id="d43ae-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="d43ae-105">Управление активами для Dynamics 365 Supply Chain Management предназначено для ведения внутренних активов.</span><span class="sxs-lookup"><span data-stu-id="d43ae-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="d43ae-106">Интеграция этих двух приложений позволяет использовать Field Service для обслуживания как активов клиентов, так и внутренних активов.</span><span class="sxs-lookup"><span data-stu-id="d43ae-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="d43ae-107">Имеется также возможность классифицировать активы на основе функционального местоположения или иерархии и отслеживать обслуживание на подробном уровне.</span><span class="sxs-lookup"><span data-stu-id="d43ae-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="d43ae-108">Дополнительные сведения см. в разделе [Интеграция Dynamics 365 Field Service и Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="d43ae-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="d43ae-109">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d43ae-109">Templates</span></span>

<span data-ttu-id="d43ae-110">Внутренние активы включают коллекцию сопоставлений основных таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d43ae-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="d43ae-111">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d43ae-111">Finance and Operations apps</span></span> | <span data-ttu-id="d43ae-112">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d43ae-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="d43ae-113">описание</span><span class="sxs-lookup"><span data-stu-id="d43ae-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="d43ae-114">Модели жизненного цикла актива в управлении активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="d43ae-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d43ae-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="d43ae-116">Состояния жизненного цикла актива в управлении активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="d43ae-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d43ae-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="d43ae-118">Активы управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-118">Asset management assets</span></span> | <span data-ttu-id="d43ae-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="d43ae-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="d43ae-120">Типы активов управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-120">Asset management asset types</span></span> | <span data-ttu-id="d43ae-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="d43ae-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="d43ae-122">Модели жизненного цикла функционального местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="d43ae-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d43ae-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="d43ae-124">Состояния жизненного цикла функционального местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="d43ae-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d43ae-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="d43ae-126">Функциональные местоположения управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-126">Asset management functional locations</span></span> | <span data-ttu-id="d43ae-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="d43ae-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="d43ae-128">Типы функциональных местоположений управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-128">Asset management functional location types</span></span> | <span data-ttu-id="d43ae-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="d43ae-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="d43ae-130">Производители управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-130">Asset management manufacturers</span></span> | <span data-ttu-id="d43ae-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="d43ae-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="d43ae-132">Модели управление активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-132">Asset management models</span></span> | <span data-ttu-id="d43ae-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="d43ae-133">msdyn\_models</span></span> | |
| <span data-ttu-id="d43ae-134">Гарантия управления активами</span><span class="sxs-lookup"><span data-stu-id="d43ae-134">Asset management warranty</span></span> | <span data-ttu-id="d43ae-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="d43ae-135">msdyn\_warranties</span></span> | |

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