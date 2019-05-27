---
title: Иерархии розничной торговли
description: В этой статье описываются иерархии розничной торговли в Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
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
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568030"
---
# <a name="retail-hierarchies"></a><span data-ttu-id="143e4-103">Иерархии розничной торговли</span><span class="sxs-lookup"><span data-stu-id="143e4-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="143e4-104">В этой статье описываются иерархии розничной торговли в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="143e4-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="143e4-105">Можно создать иерархию розничных категорий для организации продуктов, которые продаются через ваши каналы розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="143e4-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="143e4-106">Иерархии розничных продуктов можно использовать для классификации или группировки продуктов.</span><span class="sxs-lookup"><span data-stu-id="143e4-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="143e4-107">Эти продукты затем можно использовать для создания ассортиментов и программ лояльности клиентов.</span><span class="sxs-lookup"><span data-stu-id="143e4-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="143e4-108">Можно также назначить атрибуты продукции и свойства, присваивать ценовую структуру, включить продукты в специальные акции, использовать продукцию для отчетности.</span><span class="sxs-lookup"><span data-stu-id="143e4-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="143e4-109">Можно создать одну иерархию розничных категорий, чтобы представить все продукты и категории в вашей организации, а затем воспользоваться этой иерархией категорий для достижения нескольких целей.</span><span class="sxs-lookup"><span data-stu-id="143e4-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="143e4-110">Кроме того, можно создать несколько иерархий розничных категорий для специальных целей, например продвижения продукции.</span><span class="sxs-lookup"><span data-stu-id="143e4-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="143e4-111">При создании розничной иерархии продукции необходимо назначить тип иерархии категорий, чтобы обозначить цель иерархии категорий.</span><span class="sxs-lookup"><span data-stu-id="143e4-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="143e4-112">Например, только иерархии продуктов, которым назначен тип **Навигационная иерархия розничной торговли**, отображаются при просмотре продуктов по категориям через Интернет или в пункте продажи (POS).</span><span class="sxs-lookup"><span data-stu-id="143e4-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="143e4-113">Типы розничной иерархии</span><span class="sxs-lookup"><span data-stu-id="143e4-113">Retail hierarchy types</span></span>

<span data-ttu-id="143e4-114">В следующей таблице перечислены типы доступных иерархий розничных категорий и указана цель каждого типа.</span><span class="sxs-lookup"><span data-stu-id="143e4-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="143e4-115">Тип иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="143e4-115">Category hierarchy type</span></span>       | <span data-ttu-id="143e4-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="143e4-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="143e4-117">Иерархия розничных продуктов</span><span class="sxs-lookup"><span data-stu-id="143e4-117">Retail product hierarchy</span></span>      | <span data-ttu-id="143e4-118">Воспользуйтесь иерархией этого типа для определения общей иерархии продуктов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="143e4-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="143e4-119">Можно использовать данный тип иерархии для мерчендайзинга, ценообразования и специальных акций, отчетности и планирования ассортимента.</span><span class="sxs-lookup"><span data-stu-id="143e4-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="143e4-120">Только одна иерархия розничной продукции может быть присвоена этому типу иерархий.</span><span class="sxs-lookup"><span data-stu-id="143e4-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="143e4-121">Дополнительная иерархия розничной торговли</span><span class="sxs-lookup"><span data-stu-id="143e4-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="143e4-122">Этот тип иерархии используется для дополнительных иерархий розничных категорий, которые требуется создать.</span><span class="sxs-lookup"><span data-stu-id="143e4-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="143e4-123">Например, весной проводится специальная акция на купальники.</span><span class="sxs-lookup"><span data-stu-id="143e4-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="143e4-124">Таким образом, нужно включить купальники в отдельную иерархию категорий и применить рекламные цены к разным категориям продуктов этой иерархии.</span><span class="sxs-lookup"><span data-stu-id="143e4-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="143e4-125">Навигационная иерархия розничной торговли</span><span class="sxs-lookup"><span data-stu-id="143e4-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="143e4-126">Используйте этот тип иерархии, чтобы группировать и систематизировать продукты по категориям, чтобы эти продукты можно было просматривать по Интернету или в пункте продаж (POS).</span><span class="sxs-lookup"><span data-stu-id="143e4-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="143e4-127">С помощью иерархии розничных категорий можно структурировать продукты, настраивать и вести атрибуты и свойства продукции на уровне категорий.</span><span class="sxs-lookup"><span data-stu-id="143e4-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="143e4-128">Эти атрибуты и свойства включают настройки для аналитик продукции и настройки пункта продаж (POS).</span><span class="sxs-lookup"><span data-stu-id="143e4-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="143e4-129">Любые продукты, назначаемые категориям, автоматически наследуют определенные пользователем атрибуты и свойства.</span><span class="sxs-lookup"><span data-stu-id="143e4-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="143e4-130">Можно также скопировать настройки свойств любой продукции на несколько продуктов в выбранной категории одновременно.</span><span class="sxs-lookup"><span data-stu-id="143e4-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
