---
title: Отслеживание средних затрат на складскую аналитику
description: Группа складской аналитики назначается для каждой складской номенклатуры. Поэтому скользящая средняя себестоимость номенклатуры рассчитывается на основе выбранных складских аналитик, в отношении которых осуществляется финансовый контроль.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8ade2981056e9e4f49726a8c01c45f77b8e151b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "313505"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="98ff4-104">Отслеживание средних затрат на складскую аналитику</span><span class="sxs-lookup"><span data-stu-id="98ff4-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="98ff4-105">Группа складской аналитики назначается для каждой складской номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="98ff4-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="98ff4-106">Поэтому скользящая средняя себестоимость номенклатуры рассчитывается на основе выбранных складских аналитик, в отношении которых осуществляется финансовый контроль.</span><span class="sxs-lookup"><span data-stu-id="98ff4-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="98ff4-107">Существует три типа складских аналитик: по продукту, складу и отслеживанию.</span><span class="sxs-lookup"><span data-stu-id="98ff4-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="98ff4-108">Аналитики продукта включают конфигурацию, размер и цвет.</span><span class="sxs-lookup"><span data-stu-id="98ff4-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="98ff4-109">Аналитик номенклатур обязательно осуществляется финансовый контроль.</span><span class="sxs-lookup"><span data-stu-id="98ff4-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="98ff4-110">Аналитики хранения и отслеживания включают место, склад, местонахождение, статус запасов, номерной знак, номер партии и серийный номер.</span><span class="sxs-lookup"><span data-stu-id="98ff4-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="98ff4-111">Вы можете выбрать складские аналитики и аналитики отслеживания, которые будут отслеживаться по финансам.</span><span class="sxs-lookup"><span data-stu-id="98ff4-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="98ff4-112">**Пример 1**</span><span class="sxs-lookup"><span data-stu-id="98ff4-112">**Example 1**</span></span> 

<span data-ttu-id="98ff4-113">Если осуществляется финансовый контроль группы аналитики хранения, закрепленной за номенклатурой, в разрезе склада, то скользящая средняя себестоимость будет рассчитана для каждого склада.</span><span class="sxs-lookup"><span data-stu-id="98ff4-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="98ff4-114">По следующим заказам на покупки были выставлены накладные:</span><span class="sxs-lookup"><span data-stu-id="98ff4-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="98ff4-115">Для заказа на покупку в количестве 2 шт. по себестоимости USD 10,00 была создана накладная для склада GW.</span><span class="sxs-lookup"><span data-stu-id="98ff4-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="98ff4-116">Для заказа на покупку в количестве 3 шт. по себестоимости USD 12,00 была создана накладная для склада GW.</span><span class="sxs-lookup"><span data-stu-id="98ff4-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="98ff4-117">Для заказа на покупку в количестве 5 шт. по себестоимости USD 15,00 была создана накладная для склада MW.</span><span class="sxs-lookup"><span data-stu-id="98ff4-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="98ff4-118">Скользящая средняя себестоимость для склада GW равна USD 11,20, а скользящая средняя себестоимость для склада MW равна USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="98ff4-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="98ff4-119">Накладная заказа на продажу разносится для склада GW.</span><span class="sxs-lookup"><span data-stu-id="98ff4-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="98ff4-120">Стоимость запасов и себестоимость проданных товаров (до закрытия склада и без маркировки) составляет USD 11,20.</span><span class="sxs-lookup"><span data-stu-id="98ff4-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="98ff4-121">Другой заказ на продажу разносится для склада MW.</span><span class="sxs-lookup"><span data-stu-id="98ff4-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="98ff4-122">Стоимость запасов и себестоимость проданных товаров (до закрытия склада и без маркировки) составляет USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="98ff4-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="98ff4-123">**Пример 2.** Если осуществляется финансовый контроль по складам для группы аналитики хранения, закрепленной за номенклатурой, а группа аналитик отслеживания финансово отслеживается по номеру партии, скользящая средняя себестоимость вычисляется для каждой партии.</span><span class="sxs-lookup"><span data-stu-id="98ff4-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="98ff4-124">**Примечание.** Рекомендуется всегда просматривать себестоимость по всем контролируемым финансовым аналитикам.</span><span class="sxs-lookup"><span data-stu-id="98ff4-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="98ff4-125">По следующим заказам на покупки были выставлены накладные:</span><span class="sxs-lookup"><span data-stu-id="98ff4-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="98ff4-126">Для заказа на покупку в количестве 2 шт. по себестоимости USD 10,00 создана накладная для склада GW, партия ААА.</span><span class="sxs-lookup"><span data-stu-id="98ff4-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="98ff4-127">Для заказа на покупку в количестве 3 шт. по себестоимости USD 12,00 создана накладная для склада GW, партия ААА.</span><span class="sxs-lookup"><span data-stu-id="98ff4-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="98ff4-128">Для заказа на покупку в количестве 2 шт. по себестоимости USD 15,00 создана накладная для склада GW, партия BBB.</span><span class="sxs-lookup"><span data-stu-id="98ff4-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="98ff4-129">Скользящая средняя себестоимость для склада GW и партии AAA равна USD 11,20, а скользящая средняя себестоимость для склада GW и партии BBB равна USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="98ff4-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>



