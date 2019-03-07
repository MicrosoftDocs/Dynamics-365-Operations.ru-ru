---
title: Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "359252"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="42605-103">Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service</span><span class="sxs-lookup"><span data-stu-id="42605-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="42605-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="42605-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="42605-105">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="42605-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="42605-106">Используемый шаблон **Продукты Field Service (из Finance and Operations в Field Service)** основан на шаблоне **Продукты (из Finance and Operations в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="42605-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="42605-107">Дополнительные сведения см. в разделе [Продукты (из Finance and Operations в Sales) — напрямую](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="42605-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="42605-108">В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Finance and Operations в Field Service)** и **Продукты (из Finance and Operations в Field Service) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="42605-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="42605-109">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="42605-109">Templates and tasks</span></span>

<span data-ttu-id="42605-110">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="42605-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="42605-111">Продукты Field Service с единицей измерения складских запасов (из Finance and Operations в Sales)</span><span class="sxs-lookup"><span data-stu-id="42605-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="42605-112">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="42605-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="42605-113">Товары</span><span class="sxs-lookup"><span data-stu-id="42605-113">Products</span></span>

<span data-ttu-id="42605-114">Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Finance and Operations в Field Service)** включает одно сопоставление, которое не включено в шаблон **Продукты Field Service (из Finance and Operations в Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="42605-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="42605-115">Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.</span><span class="sxs-lookup"><span data-stu-id="42605-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="42605-116">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="42605-116">Template mapping in Data integration</span></span>

<span data-ttu-id="42605-117">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="42605-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="42605-118">Продукты Field Service с единицей измерения складского учета (из Finance and Operations в Field Service): Продукты</span><span class="sxs-lookup"><span data-stu-id="42605-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="42605-119">[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="42605-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
