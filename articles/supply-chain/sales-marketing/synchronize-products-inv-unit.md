---
title: Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 87daaa3d2b516581e9925fe6b769683942893ff6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206927"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="fb5e6-103">Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="fb5e6-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fb5e6-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="fb5e6-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="fb5e6-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="fb5e6-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="fb5e6-106">Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="fb5e6-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="fb5e6-107">Дополнительные сведения см. в разделе [Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="fb5e6-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="fb5e6-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="fb5e6-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="fb5e6-109">**Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)**</span><span class="sxs-lookup"><span data-stu-id="fb5e6-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="fb5e6-110">**Продукты Field Service (из Supply Chain Management в Field Service)**</span><span class="sxs-lookup"><span data-stu-id="fb5e6-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="fb5e6-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="fb5e6-111">Templates and tasks</span></span>

<span data-ttu-id="fb5e6-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="fb5e6-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="fb5e6-113">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)</span><span class="sxs-lookup"><span data-stu-id="fb5e6-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="fb5e6-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="fb5e6-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="fb5e6-115">Товары</span><span class="sxs-lookup"><span data-stu-id="fb5e6-115">Products</span></span>

<span data-ttu-id="fb5e6-116">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="fb5e6-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="fb5e6-117">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="fb5e6-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb5e6-118">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="fb5e6-118">Template mapping in Data integration</span></span>

<span data-ttu-id="fb5e6-119">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="fb5e6-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="fb5e6-120">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="fb5e6-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="fb5e6-121">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="fb5e6-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]