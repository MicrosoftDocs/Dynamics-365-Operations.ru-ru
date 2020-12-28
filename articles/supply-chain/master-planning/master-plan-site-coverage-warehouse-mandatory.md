---
title: Сводное планирование для покрытия объекта, обязательный склад
description: В этом разделе описывается, как планируется номенклатура, которая имеет объект как аналитику покрытия. Аналитика склада обязательна.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b1890f14351734c26952511f6245efe4cce5f3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436273"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="76df0-104">Сводное планирование для покрытия объекта, обязательный склад</span><span class="sxs-lookup"><span data-stu-id="76df0-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76df0-105">В этом разделе описывается, как планируется номенклатура, которая имеет объект как аналитику покрытия.</span><span class="sxs-lookup"><span data-stu-id="76df0-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="76df0-106">Аналитика склада обязательна.</span><span class="sxs-lookup"><span data-stu-id="76df0-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="76df0-107">Сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="76df0-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="76df0-108">Аналитика узла задана как обязательная и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="76df0-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="76df0-109">Этот параметр нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="76df0-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="76df0-110">Аналитика склад является обязательной и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="76df0-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="76df0-111">Аналитика узла задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="76df0-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="76df0-112">Другие аналитики также могут быть заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="76df0-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="76df0-113">Однако, они не подвержены влиянию многоузловых функций.</span><span class="sxs-lookup"><span data-stu-id="76df0-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="76df0-114">Аналитика склада не задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="76df0-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="76df0-115">Поэтому поставки и спрос объединяются узлом и, возможно, другими аналитиками планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="76df0-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="76df0-116">Следующий график иллюстрирует проведение сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="76df0-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="76df0-117">Параметры, упоминаемые на графике, и их местоположения приводятся ниже:</span><span class="sxs-lookup"><span data-stu-id="76df0-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="76df0-118">Покрытие номенклатуры определяется для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="76df0-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="76df0-119">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="76df0-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="76df0-120">Выберите номенклатуру, затем щелкните **План &gt; Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="76df0-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="76df0-121">Отношения пополнения определяются для склада.</span><span class="sxs-lookup"><span data-stu-id="76df0-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="76df0-122">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="76df0-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="76df0-123">На вкладке **Сводное планирование** см. группу поля **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="76df0-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="76df0-124">Тип заказа по умолчанию задается как производство, заказу на покупку или канбан.</span><span class="sxs-lookup"><span data-stu-id="76df0-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="76df0-125">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="76df0-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="76df0-126">Выберите номенклатуру и после этого щелкните **План &gt; Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="76df0-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="76df0-127">В форме **Параметры заказа по умолчанию** см. **Тип заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="76df0-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Спрос для склада покрытия узла обязательный](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="76df0-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="76df0-129">Additional resources</span></span>
--------

[<span data-ttu-id="76df0-130">Обзор сводного планирования и функции работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="76df0-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="76df0-131">Сводное планирование для покрытия сайта и склада, склад обязателен</span><span class="sxs-lookup"><span data-stu-id="76df0-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="76df0-132">Сводное планирование для покрытия сайта, обязательный склад</span><span class="sxs-lookup"><span data-stu-id="76df0-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="76df0-133">Сводное планирование для покрытия сайта и склада, склад не обязателен</span><span class="sxs-lookup"><span data-stu-id="76df0-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="76df0-134">Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="76df0-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



