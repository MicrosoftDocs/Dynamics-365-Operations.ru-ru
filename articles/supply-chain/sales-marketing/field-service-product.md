---
title: "Синхронизация продуктов в Finance and Operations с продуктами в Field Service"
description: "В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: ru-ru
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="484c0-103">Синхронизация продуктов в Finance and Operations с продуктами в Field Service</span><span class="sxs-lookup"><span data-stu-id="484c0-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="484c0-104">В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="484c0-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="484c0-105">Используемый шаблон **Продукты Field Service (из Fin and Ops в Field Service)** основан на шаблоне **Продукты (из Fin and Ops в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="484c0-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="484c0-106">Дополнительные сведения см. в разделе [Продукты (из Fin and Ops в Sales) — напрямую](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="484c0-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="484c0-107">В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Fin and Ops в Field Service)** и **Продукты (из Fin and Ops в Sales) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="484c0-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="484c0-108">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="484c0-108">Templates and tasks</span></span>

<span data-ttu-id="484c0-109">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="484c0-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="484c0-110">Продукты Field Service (из Fin and Ops в Field Service)</span><span class="sxs-lookup"><span data-stu-id="484c0-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="484c0-111">**Имя задачи в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="484c0-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="484c0-112">Продукты — Продукты</span><span class="sxs-lookup"><span data-stu-id="484c0-112">Products - Products</span></span>

<span data-ttu-id="484c0-113">Шаблон **Продукты Field Service (из Fin and Ops в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты (из Fin and Ops в Sales) — напрямую**.</span><span class="sxs-lookup"><span data-stu-id="484c0-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="484c0-114">Это сопоставление гарантирует, что обязательное специфичное для Field Service поле **Тип продукта Field Service** установлено правильно.</span><span class="sxs-lookup"><span data-stu-id="484c0-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="484c0-115">Используется следующее сопоставление значений.</span><span class="sxs-lookup"><span data-stu-id="484c0-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="484c0-116">В Finance and Operations значение **Тип продукта Field Service** в информационном объекте **Запущенные в производство продукты продажи** вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="484c0-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="484c0-117">**Запасы:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = True</span><span class="sxs-lookup"><span data-stu-id="484c0-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="484c0-118">**Запасы не для продажи:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = False</span><span class="sxs-lookup"><span data-stu-id="484c0-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="484c0-119">**Услуга:** Тип продукта = Услуга</span><span class="sxs-lookup"><span data-stu-id="484c0-119">**Service:** Product type = Service</span></span>

