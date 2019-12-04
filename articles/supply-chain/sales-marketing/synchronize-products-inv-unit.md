---
title: Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 18bedcc99d7d70875ec363a97e4e6eccbace3a9c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814201"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="b7481-103">Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service</span><span class="sxs-lookup"><span data-stu-id="b7481-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7481-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b7481-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="b7481-105">[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="b7481-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="b7481-106">Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="b7481-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="b7481-107">Дополнительные сведения см. в разделе [Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="b7481-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="b7481-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="b7481-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="b7481-109">**Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)**</span><span class="sxs-lookup"><span data-stu-id="b7481-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="b7481-110">**Продукты Field Service (из Supply Chain Management в Field Service)**</span><span class="sxs-lookup"><span data-stu-id="b7481-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="b7481-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="b7481-111">Templates and tasks</span></span>

<span data-ttu-id="b7481-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b7481-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="b7481-113">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)</span><span class="sxs-lookup"><span data-stu-id="b7481-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="b7481-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="b7481-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="b7481-115">Товары</span><span class="sxs-lookup"><span data-stu-id="b7481-115">Products</span></span>

<span data-ttu-id="b7481-116">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="b7481-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="b7481-117">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="b7481-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7481-118">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="b7481-118">Template mapping in Data integration</span></span>

<span data-ttu-id="b7481-119">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="b7481-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="b7481-120">Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="b7481-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="b7481-121">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="b7481-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
