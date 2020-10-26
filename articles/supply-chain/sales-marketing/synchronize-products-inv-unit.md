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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958701"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="d7b8b-103">Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="d7b8b-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d7b8b-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d7b8b-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="d7b8b-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="d7b8b-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="d7b8b-106">Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="d7b8b-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="d7b8b-107">Дополнительные сведения см. в разделе [Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="d7b8b-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="d7b8b-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="d7b8b-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="d7b8b-109">**Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)**</span><span class="sxs-lookup"><span data-stu-id="d7b8b-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="d7b8b-110">**Продукты Field Service (из Supply Chain Management в Field Service)**</span><span class="sxs-lookup"><span data-stu-id="d7b8b-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="d7b8b-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="d7b8b-111">Templates and tasks</span></span>

<span data-ttu-id="d7b8b-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="d7b8b-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="d7b8b-113">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)</span><span class="sxs-lookup"><span data-stu-id="d7b8b-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="d7b8b-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="d7b8b-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="d7b8b-115">Товары</span><span class="sxs-lookup"><span data-stu-id="d7b8b-115">Products</span></span>

<span data-ttu-id="d7b8b-116">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="d7b8b-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="d7b8b-117">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="d7b8b-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d7b8b-118">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="d7b8b-118">Template mapping in Data integration</span></span>

<span data-ttu-id="d7b8b-119">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="d7b8b-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="d7b8b-120">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="d7b8b-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="d7b8b-121">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="d7b8b-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
