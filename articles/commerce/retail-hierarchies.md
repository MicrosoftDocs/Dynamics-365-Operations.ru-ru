---
title: Иерархии Commerce
description: В этой статье описываются иерархии в Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895289"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="b08a4-103">Иерархии Commerce</span><span class="sxs-lookup"><span data-stu-id="b08a4-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b08a4-104">В этой статье описываются иерархии в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b08a4-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b08a4-105">Можно создать иерархию категорий для организации продукты, которые продаются через ваши каналы.</span><span class="sxs-lookup"><span data-stu-id="b08a4-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="b08a4-106">Иерархии продуктов можно использовать для классификации или группировки продуктов.</span><span class="sxs-lookup"><span data-stu-id="b08a4-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="b08a4-107">Эти продукты затем можно использовать для создания ассортиментов и программ лояльности клиентов.</span><span class="sxs-lookup"><span data-stu-id="b08a4-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="b08a4-108">Можно также назначить атрибуты продукции и свойства, присваивать ценовую структуру, включить продукты в специальные акции, использовать продукцию для отчетности.</span><span class="sxs-lookup"><span data-stu-id="b08a4-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="b08a4-109">Можно создать одну иерархию категорий, чтобы представить все продукты и категории в вашей организации, а затем воспользоваться этой иерархией категорий для достижения нескольких целей.</span><span class="sxs-lookup"><span data-stu-id="b08a4-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="b08a4-110">Кроме того, можно создать несколько иерархий категорий для специальных целей, например продвижения продукции.</span><span class="sxs-lookup"><span data-stu-id="b08a4-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="b08a4-111">При создании иерархии продукции необходимо назначить тип иерархии категорий, чтобы обозначить цель иерархии категорий.</span><span class="sxs-lookup"><span data-stu-id="b08a4-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="b08a4-112">Например, только иерархии продуктов, которым назначен тип **Навигационная иерархия Commerce**, отображаются при просмотре продуктов по категориям через Интернет или в пункте продажи (POS).</span><span class="sxs-lookup"><span data-stu-id="b08a4-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="b08a4-113">Типы иерархии</span><span class="sxs-lookup"><span data-stu-id="b08a4-113">Hierarchy types</span></span>

<span data-ttu-id="b08a4-114">В следующей таблице перечислены типы доступных иерархий категорий и указана цель каждого типа.</span><span class="sxs-lookup"><span data-stu-id="b08a4-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="b08a4-115">Тип иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="b08a4-115">Category hierarchy type</span></span>       | <span data-ttu-id="b08a4-116">Цель</span><span class="sxs-lookup"><span data-stu-id="b08a4-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="b08a4-117">Иерархия продуктов</span><span class="sxs-lookup"><span data-stu-id="b08a4-117">Product hierarchy</span></span>      | <span data-ttu-id="b08a4-118">Воспользуйтесь иерархией этого типа для определения общей иерархии продуктов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b08a4-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="b08a4-119">Можно использовать данный тип иерархии для мерчендайзинга, ценообразования и специальных акций, отчетности и планирования ассортимента.</span><span class="sxs-lookup"><span data-stu-id="b08a4-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="b08a4-120">Только одна иерархия продукции может быть присвоена этому типу иерархий.</span><span class="sxs-lookup"><span data-stu-id="b08a4-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="b08a4-121">Дополнительная иерархия</span><span class="sxs-lookup"><span data-stu-id="b08a4-121">Supplemental hierarchy</span></span> | <span data-ttu-id="b08a4-122">Этот тип иерархии используется для дополнительных иерархий категорий, которые требуется создать.</span><span class="sxs-lookup"><span data-stu-id="b08a4-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="b08a4-123">Например, весной проводится специальная акция на купальники.</span><span class="sxs-lookup"><span data-stu-id="b08a4-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="b08a4-124">Таким образом, нужно включить купальники в отдельную иерархию категорий и применить рекламные цены к разным категориям продуктов этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="b08a4-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="b08a4-125">Навигационная иерархия</span><span class="sxs-lookup"><span data-stu-id="b08a4-125">Navigation hierarchy</span></span>   | <span data-ttu-id="b08a4-126">Используйте этот тип иерархии, чтобы группировать и систематизировать продукты по категориям, чтобы эти продукты можно было просматривать по Интернету или в пункте продаж (POS).</span><span class="sxs-lookup"><span data-stu-id="b08a4-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="b08a4-127">С помощью иерархии категорий можно структурировать продукты, настраивать и вести атрибуты и свойства продукции на уровне категорий.</span><span class="sxs-lookup"><span data-stu-id="b08a4-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="b08a4-128">Эти атрибуты и свойства включают настройки для аналитик продукции и настройки пункта продаж (POS).</span><span class="sxs-lookup"><span data-stu-id="b08a4-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="b08a4-129">Любые продукты, назначаемые категориям, автоматически наследуют определенные пользователем атрибуты и свойства.</span><span class="sxs-lookup"><span data-stu-id="b08a4-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="b08a4-130">Можно также скопировать настройки свойств любой продукции на несколько продуктов в выбранной категории одновременно.</span><span class="sxs-lookup"><span data-stu-id="b08a4-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
