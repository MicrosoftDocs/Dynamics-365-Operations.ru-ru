---
title: "Управление категориями продуктов"
description: "В этом разделе описывается, как директора по сбыту могут использовать категории розничных продуктов для управления отношениями между иерархией розничных продуктов и сведениями о выпущенных продуктах."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: ru-ru
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="c7af2-103">Улучшенное управление продуктами и категориями</span><span class="sxs-lookup"><span data-stu-id="c7af2-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="c7af2-104">В этом разделе описывается улучшенный способ управления категориям розничных продуктов и продуктами в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c7af2-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="c7af2-105">Эти усовершенствования позволяют директорам по сбыту видеть общую структуру свойств продуктов между иерархией розничных продуктов и сведениями о выпущенных продуктах.</span><span class="sxs-lookup"><span data-stu-id="c7af2-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="c7af2-106">Для получения дополнительных сведений об управлении категориями розничных продуктов выберите **Иерархия розничных продуктов** в рабочей области **Управление категориями и продуктами** и обратите внимание на улучшенную структуру страницы **Категория розничных продуктов**.</span><span class="sxs-lookup"><span data-stu-id="c7af2-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Рабочая область управления категориями и продуктами](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="c7af2-108">В предыдущих версиях свойства продукта делились на **Базовые свойства продукта** и **Свойства розничного продукта** в зависимости от области их применимости.</span><span class="sxs-lookup"><span data-stu-id="c7af2-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="c7af2-109">**Свойства розничного продукта** были *глобальными* по области применимости, что означает, что для конкретного **Свойства розничного продукта** одно и то же значение совместно используется всеми юридическими лицами.</span><span class="sxs-lookup"><span data-stu-id="c7af2-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="c7af2-110">**Базовые свойства продукта** связаны с *конкретным юридическим лицом*.</span><span class="sxs-lookup"><span data-stu-id="c7af2-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="c7af2-111">Иными словами, значение конкретного **Базового свойства продукта** в разных юридических лицах может иметь разные значения в зависимости от индивидуальных бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="c7af2-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="c7af2-112">В усовершенствованной структуре категорий розничных продуктов свойств продуктов логически разделены на основании их применимости внутри группы, чтобы отразить структуру формы сведений о выпущенном продукте.</span><span class="sxs-lookup"><span data-stu-id="c7af2-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Группирование полей в зависимости от области их применимости](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="c7af2-114">Можно переключаться между управлением свойствами, связанными с конкретным юридическим лицом, по всем юридическим лицам и управлением ими для конкретного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="c7af2-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="c7af2-115">Чтобы сделать это, выберите **Просмотр/изменение для всех юридических лиц** или **Просмотр/изменение для конкретного юридического лица**.</span><span class="sxs-lookup"><span data-stu-id="c7af2-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Переключение между отдельным юридическим лицом и всеми юридическими лицами](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Переключение между отдельным юридическим лицом и всеми юридическими лицами](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="c7af2-118">По сравнению с предыдущими версиями, в новой структуре категорий розничных продуктов директор по сбыту можно также определить значения по умолчанию для дополнительного набора свойства продуктов на уровне отдельных категорий.</span><span class="sxs-lookup"><span data-stu-id="c7af2-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="c7af2-119">Во время создания продукта эти значения свойств продукта по умолчанию наследуются продуктом на основании его связи с отдельной категорией из иерархии розничных продуктов.</span><span class="sxs-lookup"><span data-stu-id="c7af2-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="c7af2-120">Эти наследуемые свойства продуктов также могут быть изменены для каждого продукта в соответствии с индивидуальными бизнес-требованиями.</span><span class="sxs-lookup"><span data-stu-id="c7af2-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="c7af2-121">Выбор свойств для обновления продуктов из формы "Категория розничных продуктов"</span><span class="sxs-lookup"><span data-stu-id="c7af2-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="c7af2-122">Можно использовать эту новую улучшенную структуру свойств продукта для выбора того, какие обновленные свойства продукта должны принудительно передаваться в соответствующие продукты.</span><span class="sxs-lookup"><span data-stu-id="c7af2-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Новое улучшенное представление обновления продуктов](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="c7af2-124">Директоры по сбыту могут изменять эти наследуемые свойства продуктов для каждого продукта в соответствии с индивидуальными бизнес-требованиями.</span><span class="sxs-lookup"><span data-stu-id="c7af2-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


