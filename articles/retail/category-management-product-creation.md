---
title: Управление категориям розничных продуктов и продуктами
description: В этом разделе описывается, как директора по сбыту могут использовать категории розничных продуктов для управления отношениями между иерархией розничных продуктов и сведениями о выпущенных продуктах.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "344693"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="d6437-103">Управление категориям розничных продуктов и продуктами</span><span class="sxs-lookup"><span data-stu-id="d6437-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="d6437-104">В этом разделе описывается улучшенный способ управления категориям розничных продуктов и продуктами в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d6437-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d6437-105">Эти усовершенствования позволяют директорам по сбыту видеть структуру свойств продуктов, которая является общей между иерархией розничных продуктов и сведениями о выпущенных продуктах.</span><span class="sxs-lookup"><span data-stu-id="d6437-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="d6437-106">Для получения дополнительных сведений об управлении розничными категориями продуктов в рабочей области **Управление категориями и продуктами** выберите плитку **Иерархия розничных продуктов**.</span><span class="sxs-lookup"><span data-stu-id="d6437-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="d6437-107">Обратите внимание на улучшенную структуру страницы **Иерархия розничных продуктов**, которая отображается.</span><span class="sxs-lookup"><span data-stu-id="d6437-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="d6437-108">В предыдущих версиях Retail свойства продукта делились на *базовые свойства продукта* и *свойства розничного продукта* в зависимости от области их применимости.</span><span class="sxs-lookup"><span data-stu-id="d6437-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="d6437-109">Свойства розничного продукта являются *глобальными* в области их применимости.</span><span class="sxs-lookup"><span data-stu-id="d6437-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="d6437-110">Иными словами, для определенного свойства розничного продукта во всех юридических лицах используется одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="d6437-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d6437-111">Напротив, базовые свойства продукта связаны с *конкретным юридическим лицом*.</span><span class="sxs-lookup"><span data-stu-id="d6437-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="d6437-112">Иными словами, значение конкретного базового свойства продукта в разных юридических лицах может иметь разные значения в зависимости от индивидуальных бизнес-требований каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="d6437-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="d6437-113">В усовершенствованной структуре категорий розничных продуктов свойств продуктов логически разделены на основании их применимости внутри группы, чтобы отразить структуру формы сведений о выпущенном продукте.</span><span class="sxs-lookup"><span data-stu-id="d6437-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Поля группируются в зависимости от области применимости свойств](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d6437-115">Можно переключаться между управлением свойствами, связанными с конкретным юридическим лицом, по всем юридическим лицам и управлением ими для конкретного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="d6437-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="d6437-116">Чтобы управлять свойствами во всех юридических лицах, выберите **Просмотр для всех юридических лиц** (или **Изменение для всех юридических лиц**).</span><span class="sxs-lookup"><span data-stu-id="d6437-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Просмотр/изменение для всех юридических лиц](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="d6437-118">Чтобы управлять свойствами для конкретного юридического лица, выберите **Просмотр для конкретного юридического лица** (или **Изменение для конкретного юридического лица**).</span><span class="sxs-lookup"><span data-stu-id="d6437-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Просмотр/изменение для конкретного юридического лица](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="d6437-120">Кроме того, в улучшенной структуре категорий розничных продуктов директор по сбыту может теперь также определить значения по умолчанию для дополнительного набора свойства продуктов на уровне отдельных категорий.</span><span class="sxs-lookup"><span data-stu-id="d6437-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="d6437-121">Затем при создании продуктов они наследуют значения по умолчанию для своих свойств продукта на основе связи этих свойств с отдельной категорией из иерархии розничных продуктов.</span><span class="sxs-lookup"><span data-stu-id="d6437-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="d6437-122">Эти наследуемые свойства продуктов также могут быть изменены для каждого продукта в соответствии с индивидуальными бизнес-требованиями.</span><span class="sxs-lookup"><span data-stu-id="d6437-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="d6437-123">Выбор свойств для обновления продуктов на странице "Категория розничных продуктов"</span><span class="sxs-lookup"><span data-stu-id="d6437-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="d6437-124">Можно использовать эту новую улучшенную структуру свойств продукта для выбора того, какие обновленные свойства продукта должны принудительно передаваться в соответствующие продукты.</span><span class="sxs-lookup"><span data-stu-id="d6437-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="d6437-125">На странице **Иерархия розничных продуктов** в области действий выберите **Категория**, затем выберите **Обновить продукты** для открытия диалогового окна **Обновить продукты**.</span><span class="sxs-lookup"><span data-stu-id="d6437-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Диалоговое окно обновления продуктов](media/NewUpdateProductsEnhancedView.PNG)
