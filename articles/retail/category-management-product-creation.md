---
title: "Управление категориями продуктов и их создание"
description: "В этой теме описываются усовершенствования, внесенные в функциональность управления категориями розничных продуктов. Эти усовершенствования позволяют директорам по сбыту видеть корреляцию между иерархией розничных продуктов и сведениями об используемых продуктах."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="1b38d-104">Управление категориями продуктов и их создание</span><span class="sxs-lookup"><span data-stu-id="1b38d-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="1b38d-105">Усовершенствования, внесенные в функциональность управления категориями розничных продуктов, позволяют директорам по сбыту видеть корреляцию между иерархией розничных продуктов и сведениями об используемых продуктах.</span><span class="sxs-lookup"><span data-stu-id="1b38d-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="1b38d-106">Для просмотра этих усовершенствований в рабочей области **Управление категориями и продуктами** выберите **Иерархия розничных продуктов**, чтобы открыть страницу **Новая структура категории розничных продуктов**.</span><span class="sxs-lookup"><span data-stu-id="1b38d-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="1b38d-107">В предыдущих выпусках свойства продукта делились на базовые свойства продукта и свойства розничного продукта в зависимости от области их применимости.</span><span class="sxs-lookup"><span data-stu-id="1b38d-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="1b38d-108">Свойства розничного продукта были *глобальными*.</span><span class="sxs-lookup"><span data-stu-id="1b38d-108">Retail product properties were *global*.</span></span> <span data-ttu-id="1b38d-109">Иными словами, для свойства продукта во всех юридических лицах используется одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="1b38d-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="1b38d-110">Базовые свойства продукта были *связаны с конкретным юридическим лицом*.</span><span class="sxs-lookup"><span data-stu-id="1b38d-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="1b38d-111">Иными словами, свойство продукта в разных юридических лицах может иметь разные значения в зависимости от индивидуальных бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="1b38d-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="1b38d-112">В этих усовершенствованиях для свойств продуктов в категории розничных продуктов мы продолжаем разделять поля на основании них применимости внутри группы, чтобы отразить структуру формы сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="1b38d-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="1b38d-113">Можно переключаться между управлением свойствами, связанными с конкретным юридическим лицом, по всем юридическим лицам и управлением ими для конкретного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="1b38d-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="1b38d-114">Просто выберите **Просмотр/изменение для всех юридических лиц** или **Просмотр/изменение для конкретного юридического лица**.</span><span class="sxs-lookup"><span data-stu-id="1b38d-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="1b38d-115">Директоры по сбыту также могут задавать значения по умолчанию для дополнительного набора свойств продуктов на уровне отдельной категории.</span><span class="sxs-lookup"><span data-stu-id="1b38d-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="1b38d-116">Эти значения свойств наследуются продуктами в зависимости от их связи с категорией в момент создания продукта.</span><span class="sxs-lookup"><span data-stu-id="1b38d-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="1b38d-117">Выбор свойств для обновления продуктов из формы "Категория розничных продуктов"</span><span class="sxs-lookup"><span data-stu-id="1b38d-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="1b38d-118">Вы можете использовать свойства логической группировки свойств, чтобы выбрать, какие обновленные свойства продукта должны отправляться в связанные продукты.</span><span class="sxs-lookup"><span data-stu-id="1b38d-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="1b38d-119">Директоры по сбыту могут изменять эти наследуемые свойства продуктов для каждого продукта в соответствии с индивидуальными бизнес-требованиями.</span><span class="sxs-lookup"><span data-stu-id="1b38d-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

