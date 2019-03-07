---
title: Подтверждение продукта для комплектации кластера
description: В этом разделе описывается настройка проверки номенклатуры вместе с комплектацией кластера.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d2ce787e6a7d677bc997bff363f34850ff9899b
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "338115"
---
[!include [banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="544c3-103">Подтверждение продукта для комплектации кластера</span><span class="sxs-lookup"><span data-stu-id="544c3-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="544c3-104">Комплектация кластера позволяет скомплектовать номенклатуры для нескольких заказов одновременно.</span><span class="sxs-lookup"><span data-stu-id="544c3-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="544c3-105">При применении комплектации кластера критически важно подтверждение номенклатуры для проверки номенклатур, которые добавляются в кластеры.</span><span class="sxs-lookup"><span data-stu-id="544c3-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="544c3-106">Вы можете проверить номенклатуры в комплектации кластера во время процесса комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="544c3-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="544c3-107">Где применяется.</span><span class="sxs-lookup"><span data-stu-id="544c3-107">Where it applies</span></span>
<span data-ttu-id="544c3-108">Проверка номенклатуры для комплектации кластера работает так же, как при проверьте номенклатур в процессе комплектации без кластера.</span><span class="sxs-lookup"><span data-stu-id="544c3-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="544c3-109">Настройка основана на настройке штрих-кода продукта.</span><span class="sxs-lookup"><span data-stu-id="544c3-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="544c3-110">Настройка проверки номенклатуры с комплектацией кластера</span><span class="sxs-lookup"><span data-stu-id="544c3-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="544c3-111">В меню мобильного устройства откройте форму настройки для подтверждения работы: **Управление складом** > **Управление складом** > **Настройки** > **Мобильное устройство** > **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="544c3-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="544c3-112">В пунктах меню мобильного устройства откройте **Настройка подтверждения работы**.</span><span class="sxs-lookup"><span data-stu-id="544c3-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="544c3-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="544c3-113">Option</span></span>        |                                    <span data-ttu-id="544c3-114">описание</span><span class="sxs-lookup"><span data-stu-id="544c3-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="544c3-115">Подтверждение продукта</span><span class="sxs-lookup"><span data-stu-id="544c3-115">Product confirmation</span></span> | <span data-ttu-id="544c3-116">Можно подтвердить каждую позицию запасов с мобильного устройства при сканировании.</span><span class="sxs-lookup"><span data-stu-id="544c3-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

