---
title: "Подтверждение продукта для комплектации кластера"
description: "В этом разделе описывается настройка проверки номенклатуры вместе с комплектацией кластера."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 17f5761df4294abfea28e7cb8d50c86f1e3e136f
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

[!include[banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="e3d22-103">Подтверждение продукта для комплектации кластера</span><span class="sxs-lookup"><span data-stu-id="e3d22-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="e3d22-104">Комплектация кластера позволяет скомплектовать номенклатуры для нескольких заказов одновременно.</span><span class="sxs-lookup"><span data-stu-id="e3d22-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="e3d22-105">При применении комплектации кластера критически важно подтверждение номенклатуры для проверки номенклатур, которые добавляются в кластеры.</span><span class="sxs-lookup"><span data-stu-id="e3d22-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="e3d22-106">Вы можете проверить номенклатуры в комплектации кластера во время процесса комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="e3d22-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e3d22-107">Где применяется.</span><span class="sxs-lookup"><span data-stu-id="e3d22-107">Where it applies</span></span>
<span data-ttu-id="e3d22-108">Проверка номенклатуры для комплектации кластера работает так же, как при проверьте номенклатур в процессе комплектации без кластера.</span><span class="sxs-lookup"><span data-stu-id="e3d22-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="e3d22-109">Настройка основана на настройке штрих-кода продукта.</span><span class="sxs-lookup"><span data-stu-id="e3d22-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="e3d22-110">Настройка проверки номенклатуры с комплектацией кластера</span><span class="sxs-lookup"><span data-stu-id="e3d22-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="e3d22-111">В меню мобильного устройства откройте форму настройки для подтверждения работы: **Управление складом** > **Управление складом** > **Настройки** > **Мобильное устройство** > **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="e3d22-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="e3d22-112">В пунктах меню мобильного устройства откройте **Настройка подтверждения работы**.</span><span class="sxs-lookup"><span data-stu-id="e3d22-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

| <span data-ttu-id="e3d22-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="e3d22-113">Option</span></span>        | <span data-ttu-id="e3d22-114">описание</span><span class="sxs-lookup"><span data-stu-id="e3d22-114">Description</span></span>   | 
| ------------- | ------------- |
|<span data-ttu-id="e3d22-115">Подтверждение продукта</span><span class="sxs-lookup"><span data-stu-id="e3d22-115">Product confirmation</span></span> | <span data-ttu-id="e3d22-116">Можно подтвердить каждую позицию запасов с мобильного устройства при сканировании.</span><span class="sxs-lookup"><span data-stu-id="e3d22-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span>|

