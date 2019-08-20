---
title: Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835702"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="147aa-103">Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service</span><span class="sxs-lookup"><span data-stu-id="147aa-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="147aa-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="147aa-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="147aa-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="147aa-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="147aa-106">Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** основан на шаблоне **Продукты Field Service (из Fin and Ops в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="147aa-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="147aa-107">Дополнительные сведения см. в разделе [Продукты Field Service (из Finance and Operations в Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="147aa-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="147aa-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="147aa-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="147aa-109">**Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)**</span><span class="sxs-lookup"><span data-stu-id="147aa-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="147aa-110">**Продукты Field Service (из Fin and Ops в Field Service)**</span><span class="sxs-lookup"><span data-stu-id="147aa-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="147aa-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="147aa-111">Templates and tasks</span></span>

<span data-ttu-id="147aa-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="147aa-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="147aa-113">Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="147aa-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="147aa-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="147aa-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="147aa-115">Товары</span><span class="sxs-lookup"><span data-stu-id="147aa-115">Products</span></span>

<span data-ttu-id="147aa-116">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** включает одно сопоставление, которое не включено в шаблон **Продукты Field Service (из Fin and Ops в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="147aa-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="147aa-117">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="147aa-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="147aa-118">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="147aa-118">Template mapping in Data integration</span></span>

<span data-ttu-id="147aa-119">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="147aa-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="147aa-120">Продукты Field Service с единицей измерения складского учета (из Fin and Ops в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="147aa-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="147aa-121">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="147aa-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
