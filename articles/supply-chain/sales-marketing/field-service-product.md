---
title: Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service
description: В этом разделе описываются шаблоны и базовая задача, которые используются для синхронизации продуктов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436200"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="1d6ab-103">Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service</span><span class="sxs-lookup"><span data-stu-id="1d6ab-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1d6ab-104">В этой теме рассматриваются шаблоны и базовая задача, которые используются для синхронизации продуктов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="1d6ab-105">Используемый шаблон **Продукты Field Service (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты (из Supply Chain Management в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="1d6ab-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="1d6ab-106">Дополнительные сведения см. в разделе [Продукты (из Supply Chain Management в Sales) — напрямую](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="1d6ab-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="1d6ab-107">В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Supply Chain Management в Field Service)** и **Продукты (из Supply Chain Management в Sales) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1d6ab-108">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="1d6ab-108">Templates and tasks</span></span>

<span data-ttu-id="1d6ab-109">**Имя шаблона в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="1d6ab-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="1d6ab-110">Продукты Field Service (из Supply Chain Management в Field Service)</span><span class="sxs-lookup"><span data-stu-id="1d6ab-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="1d6ab-111">**Имя задачи в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="1d6ab-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="1d6ab-112">Продукты — Продукты</span><span class="sxs-lookup"><span data-stu-id="1d6ab-112">Products - Products</span></span>

<span data-ttu-id="1d6ab-113">Шаблон **Продукты Field Service (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты (из Supply Chain Management в Sales) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="1d6ab-114">Это сопоставление гарантирует, что обязательное специфичное для Field Service поле **Тип продукта Field Service** установлено правильно.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="1d6ab-115">Используется следующее сопоставление значений.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="1d6ab-116">В Supply Chain Management значение **Тип продукта Field Service** в информационном объекте **Запущенные в производство продукты продажи** вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1d6ab-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="1d6ab-117">**Запасы:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = True</span><span class="sxs-lookup"><span data-stu-id="1d6ab-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="1d6ab-118">**Запасы не для продажи:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = False</span><span class="sxs-lookup"><span data-stu-id="1d6ab-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="1d6ab-119">**Услуга:** Тип продукта = Услуга</span><span class="sxs-lookup"><span data-stu-id="1d6ab-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1d6ab-120">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="1d6ab-120">Template mapping in Data integration</span></span>

<span data-ttu-id="1d6ab-121">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="1d6ab-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="1d6ab-122">Продукты Field Service (из Supply Chain Management в Field Service): Продукты — Продукты</span><span class="sxs-lookup"><span data-stu-id="1d6ab-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="1d6ab-123">[![Сопоставление шаблона в интеграции данных](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="1d6ab-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
