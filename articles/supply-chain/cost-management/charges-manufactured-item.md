---
title: "Отображение накладных расходов для производимой номенклатуры"
description: "Постоянные затраты по произведенной номенклатуре отражают время настройки операции и компоненты, имеющие постоянное количество или сумму постоянных отходов."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b8fcfc1a9386d05c2adbcb4208e7ef5d01644430
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="25e12-103">Отображение накладных расходов для производимой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="25e12-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25e12-104">Постоянные затраты по произведенной номенклатуре отражают время настройки операции и компоненты, имеющие постоянное количество или сумму постоянных отходов.</span><span class="sxs-lookup"><span data-stu-id="25e12-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="25e12-105">Вычисленная сумма накладных расходов по номенклатуре может отображаться вместе с затратами на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25e12-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="25e12-106">Однако накладные расходы иногда отображаются в виде отдельных полей, и не включаются в затраты на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25e12-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="25e12-107">Когда накладные расходы отображаются как отдельные поля, одно поле содержит общую сумму накладных расходов, а другие поля содержат размер лота затрат, который используется для амортизации суммы.</span><span class="sxs-lookup"><span data-stu-id="25e12-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="25e12-108">На странице "Цена номенклатуры", например, накладные расходы отображаются в 2 отдельных полях.</span><span class="sxs-lookup"><span data-stu-id="25e12-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="25e12-109">Однако страница "Выполнить" содержит итоговые затраты на единицу измерения, и амортизированные затраты включаются в затраты на единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="25e12-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="25e12-110">Для целей расчета стандартных затрат накладные расходы для произведенной номенклатуры всегда включаются в затраты на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25e12-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="25e12-111">Дополнительно накладные расходы могут быть включены для целей расчета плановых затрат.</span><span class="sxs-lookup"><span data-stu-id="25e12-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="25e12-112">Политика в рамках версии обеспечивает принудительное включение накладных расходов в затраты по произведенной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="25e12-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="25e12-113">Активация записи затрат по номенклатуре приводит к обновлению накладных расходов в составе сведений о базовых затратах по номенклатуре, которая отображается на странице "Цена номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="25e12-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="25e12-114">Накладные расходы отображаются в двух отдельных полях и не включаются в затраты на единицу измерения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="25e12-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="25e12-115">Каждая активация обновляет сведения о базовых затратах по номенклатуре, даже если активация отражает различные узлы.</span><span class="sxs-lookup"><span data-stu-id="25e12-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="25e12-116">Следовательно, сведения о базовых затратах следует рассматривать как справочную информацию.</span><span class="sxs-lookup"><span data-stu-id="25e12-116">Therefore, you should view the base cost information as reference information.</span></span>






