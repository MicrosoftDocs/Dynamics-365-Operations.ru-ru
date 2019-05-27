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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535867"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="95eb6-103">Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service</span><span class="sxs-lookup"><span data-stu-id="95eb6-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="95eb6-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="95eb6-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="95eb6-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="95eb6-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="95eb6-106">Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** основан на шаблоне **Продукты Field Service (из Fin and Ops в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="95eb6-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="95eb6-107">Дополнительные сведения см. в разделе [Продукты Field Service (из Finance and Operations в Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="95eb6-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="95eb6-108">В этом разделе описываются только различия между двумя шаблонами:</span><span class="sxs-lookup"><span data-stu-id="95eb6-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="95eb6-109">**Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)**</span><span class="sxs-lookup"><span data-stu-id="95eb6-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="95eb6-110">**Продукты Field Service (из Fin and Ops в Field Service)**</span><span class="sxs-lookup"><span data-stu-id="95eb6-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="95eb6-111">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="95eb6-111">Templates and tasks</span></span>

<span data-ttu-id="95eb6-112">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="95eb6-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="95eb6-113">Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="95eb6-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="95eb6-114">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="95eb6-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="95eb6-115">Товары</span><span class="sxs-lookup"><span data-stu-id="95eb6-115">Products</span></span>

<span data-ttu-id="95eb6-116">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** включает одно сопоставление, которое не включено в шаблон **Продукты Field Service (из Fin and Ops в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="95eb6-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="95eb6-117">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="95eb6-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="95eb6-118">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="95eb6-118">Template mapping in Data integration</span></span>

<span data-ttu-id="95eb6-119">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="95eb6-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="95eb6-120">Продукты Field Service с единицей измерения складского учета (из Fin and Ops в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="95eb6-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="95eb6-121">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="95eb6-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
