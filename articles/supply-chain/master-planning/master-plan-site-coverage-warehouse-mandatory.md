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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977971"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="2f099-104">Сводное планирование для покрытия объекта, обязательный склад</span><span class="sxs-lookup"><span data-stu-id="2f099-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f099-105">В этом разделе описывается, как планируется номенклатура, которая имеет объект как аналитику покрытия.</span><span class="sxs-lookup"><span data-stu-id="2f099-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="2f099-106">Аналитика склада обязательна.</span><span class="sxs-lookup"><span data-stu-id="2f099-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="2f099-107">Сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="2f099-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="2f099-108">Аналитика узла задана как обязательная и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="2f099-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="2f099-109">Этот параметр нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="2f099-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="2f099-110">Аналитика склад является обязательной и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="2f099-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="2f099-111">Аналитика узла задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="2f099-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="2f099-112">Другие аналитики также могут быть заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="2f099-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="2f099-113">Однако, они не подвержены влиянию многоузловых функций.</span><span class="sxs-lookup"><span data-stu-id="2f099-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="2f099-114">Аналитика склада не задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="2f099-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="2f099-115">Поэтому поставки и спрос объединяются узлом и, возможно, другими аналитиками планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="2f099-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="2f099-116">Следующий график иллюстрирует проведение сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="2f099-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="2f099-117">Параметры, упоминаемые на графике, и их местоположения приводятся ниже:</span><span class="sxs-lookup"><span data-stu-id="2f099-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="2f099-118">Покрытие номенклатуры определяется для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="2f099-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="2f099-119">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="2f099-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2f099-120">Выберите номенклатуру, затем щелкните **План &gt; Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="2f099-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="2f099-121">Отношения пополнения определяются для склада.</span><span class="sxs-lookup"><span data-stu-id="2f099-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="2f099-122">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="2f099-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="2f099-123">На вкладке **Сводное планирование** см. группу поля **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="2f099-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="2f099-124">Тип заказа по умолчанию задается как производство, заказу на покупку или канбан.</span><span class="sxs-lookup"><span data-stu-id="2f099-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="2f099-125">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="2f099-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2f099-126">Выберите номенклатуру и после этого щелкните **План &gt; Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="2f099-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="2f099-127">В форме **Параметры заказа по умолчанию** см. **Тип заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="2f099-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Спрос для склада покрытия узла обязательный](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="2f099-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f099-129">Additional resources</span></span>
--------

[<span data-ttu-id="2f099-130">Обзор сводного планирования и функции работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="2f099-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="2f099-131">Сводное планирование для покрытия сайта и склада, склад обязателен</span><span class="sxs-lookup"><span data-stu-id="2f099-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2f099-132">Сводное планирование для покрытия сайта, обязательный склад</span><span class="sxs-lookup"><span data-stu-id="2f099-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2f099-133">Сводное планирование для покрытия сайта и склада, склад не обязателен</span><span class="sxs-lookup"><span data-stu-id="2f099-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="2f099-134">Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="2f099-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



