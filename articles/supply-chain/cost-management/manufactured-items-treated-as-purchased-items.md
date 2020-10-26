---
title: Настройка продуктов, которые можно произвести или приобрести
description: Продукты могут получаться из различных источников — их можно произвести (изготовить) или приобрести (купить). В этой статье описываются некоторые типичные моменты, которые следует учитывать при настройке продуктов для поддержки нескольких источника.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9b5ba58703e636308d83a94ecc2e27e44812c49
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981543"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="f899d-104">Настройка продуктов, которые можно произвести или приобрести</span><span class="sxs-lookup"><span data-stu-id="f899d-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f899d-105">Продукты могут получаться из различных источников — их можно произвести (изготовить) или приобрести (купить).</span><span class="sxs-lookup"><span data-stu-id="f899d-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="f899d-106">В этой статье описываются некоторые типичные моменты, которые следует учитывать при настройке продуктов для поддержки нескольких источника.</span><span class="sxs-lookup"><span data-stu-id="f899d-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="f899d-107">Несколько источников обычно используется для покупной номенклатуры, которая иногда изготавливается, или когда номенклатура, которая раньше обычно изготавливалась, изменена таким образом, что теперь она в основном закупается.</span><span class="sxs-lookup"><span data-stu-id="f899d-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="f899d-108">Сначала номенклатура указывается как произведенная номенклатура, чтобы можно было определить спецификацию и данные маршрута и обеспечить поддержку производственных заказов на номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="f899d-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="f899d-109">Для типа производства должно быть установлено значение **Спецификация** (или, для непрерывного производства, **Формула** или **Сопутствующий продукт**).</span><span class="sxs-lookup"><span data-stu-id="f899d-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="f899d-110">Когда вы используете стандартную себестоимость, запись стоимости номенклатуры может быть рассчитана для изготовленной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f899d-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="f899d-111">Однако запись стоимости номенклатуры может не соответствовать стандартной себестоимости, которая требуется для целей закупки.</span><span class="sxs-lookup"><span data-stu-id="f899d-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="f899d-112">В таком случае стандартную себестоимость нужно ввести вручную и активировать для записи по себестоимости номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f899d-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="f899d-113">Для вычисления стоимости рассмотрите использование специальной спецификации и маршрута, которые представляют смесь поставок продукта в течение финансового периода, чтобы уменьшить отклонения с течением времени.</span><span class="sxs-lookup"><span data-stu-id="f899d-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="f899d-114">Кроме того, произведенную номенклатуру на одном сайте можно перенести на другой сайт.</span><span class="sxs-lookup"><span data-stu-id="f899d-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="f899d-115">Поэтому стоимость номенклатуры необходимо вводить вручную и активировать для сайта, куда номенклатура перемещается.</span><span class="sxs-lookup"><span data-stu-id="f899d-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="f899d-116">При использовании произведенной номенклатуры в качестве компонента продуктов более высокого уровня затраты на компонент должны рассматриваться как приобретенная номенклатура.</span><span class="sxs-lookup"><span data-stu-id="f899d-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="f899d-117">Эта рекомендация действует независимо от того, рассчитывались ли затраты или вводились вручную.</span><span class="sxs-lookup"><span data-stu-id="f899d-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="f899d-118">Другими словами, в расчете спецификации затраты на номенклатуру должны рассматриваться как приобретенный компонент вместо использования сведений о спецификации и маршруте для расчета затрат.</span><span class="sxs-lookup"><span data-stu-id="f899d-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="f899d-119">Во избежание выполнения этого расчета, выберите флага **Остановка развертывания**, который внедрен в группу расчета спецификации, назначенную этой номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="f899d-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="f899d-120">Для предотвращения развертывания требований номенклатуры при подсчете сводного планирования, задайте границу развертывания, равную 0 (нулю) дней, в покрытии номенклатуры или в группе покрытия.</span><span class="sxs-lookup"><span data-stu-id="f899d-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="f899d-121">Расчет свободного планирования будет затем рассматривать номенклатуру как купленную номенклатуру и не будет производить дальнейшие расчеты по данным спецификации и маршрута номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f899d-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





