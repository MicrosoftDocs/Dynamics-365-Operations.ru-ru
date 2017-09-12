---
title: "Амортизация постоянных затрат для производимой номенклатуры"
description: "Постоянные затраты по произведенной номенклатуре отражают время настройки операции и компоненты, имеющие постоянное количество или постоянную сумму отходов."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8c72cf675d99f78c03ae2f2fef53b51fbf4bd8b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="51c2d-103">Амортизация постоянных затрат для производимой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="51c2d-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="51c2d-104">Постоянные затраты по произведенной номенклатуре отражают время настройки операции и компоненты, имеющие постоянное количество или постоянную сумму отходов.</span><span class="sxs-lookup"><span data-stu-id="51c2d-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="51c2d-105">Понятие "размер лота затрат" используется для амортизации этих постоянных затрат в составе вычисленных затрат по произведенной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="51c2d-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="51c2d-106">Эта понятие имеет несколько синонимов, одним из которых является "размер учетного лота".</span><span class="sxs-lookup"><span data-stu-id="51c2d-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="51c2d-107">Понятие "амортизационные постоянные затраты" также имеет несколько синонимов, одним из которых является "пропорциональные постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="51c2d-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>
<span data-ttu-id="51c2d-108">Количество размера лота затрат по произведенной номенклатуре используется при расчете спецификации.</span><span class="sxs-lookup"><span data-stu-id="51c2d-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="51c2d-109">Количество зависит от способа инициирования и выполнения расчета спецификации, что иллюстрируется следующим:</span><span class="sxs-lookup"><span data-stu-id="51c2d-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>
-   <span data-ttu-id="51c2d-110">Расчетное количество по умолчанию при расчете спецификации по номенклатуре. В качестве значения по умолчанию для размера лота затрат по данной номенклатуре выступает стандартное количество заказа по номенклатуре для складских запасов, но значение по умолчанию может представлять собой большее количество, кратное количеству заказа по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="51c2d-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="51c2d-111">Стандартное количество заказа по номенклатуре и кратное количество могут быть определены в параметрах по умолчанию заказа по номенклатуре или в параметрах заказа для определенного узла.</span><span class="sxs-lookup"><span data-stu-id="51c2d-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="51c2d-112">Указанное расчетное количество при расчете спецификации по номенклатуре ? Указанное расчетное количество выступает в качестве размера лота затрат по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="51c2d-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="51c2d-113">По умолчанию расчетное количество первоначально равно стандартному количеству заказа по номенклатуре, но оно может быть переопределено вручную.</span><span class="sxs-lookup"><span data-stu-id="51c2d-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="51c2d-114">Указанное расчетное количество представляет собой размер лота затрат для указанной номенклатуры и для произведенных компонентов со строкой спецификации, относящейся к типу "Производство".</span><span class="sxs-lookup"><span data-stu-id="51c2d-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="51c2d-115">Это необходимо, поскольку предполагается, что будет произведено точное количество компонента.</span><span class="sxs-lookup"><span data-stu-id="51c2d-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="51c2d-116">Размер лота затрат для других произведенных компонентов со строкой спецификации, относящейся к типу "Номенклатура", будет отражать стандартное количество заказа по этим номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="51c2d-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="51c2d-117">Указанное для изготовления на заказ расчетное количество при расчете спецификации по номенклатуре ? Указанное расчетное количество выступает в качестве размера лота затрат для номенклатуры и произведенных компонентов номенклатуры, когда при расчете спецификации используется режим развертывания под заказ.</span><span class="sxs-lookup"><span data-stu-id="51c2d-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="51c2d-118">Предполагается, что произведенные компоненты будут изготовлены в точном количестве, точно также как и произведенные компоненты со строкой спецификации, относящейся к типу "Производство".</span><span class="sxs-lookup"><span data-stu-id="51c2d-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="51c2d-119">Указанное расчетное количество при расчете спецификации для определенного заказа. Расчет спецификации для определенного заказа может быть выполнен для номенклатуры строки в заказе на продажу, предложении по продаже или заказе на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="51c2d-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="51c2d-120">Указанное расчетное количество использует количество для номенклатуры исходной строки, но количество по умолчанию можно переопределить.</span><span class="sxs-lookup"><span data-stu-id="51c2d-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="51c2d-121">Можно выбрать, будет ли при расчете спецификации для определенного заказа использоваться режим развертывания под заказ или многоуровневый режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="51c2d-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="51c2d-122">Вычисленная сумма амортизированных постоянных затрат по произведенной номенклатуре называется расходами.</span><span class="sxs-lookup"><span data-stu-id="51c2d-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






