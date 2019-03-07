---
title: Сводное планирование для покрытия объекта и склада, склад является обязательным
description: В этом разделе описывается, как планируется номенклатура, которая имеет место и склад в качестве аналитики покрытия. Аналитика склада обязательна.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52fc9955afe2a7502d0e1f9e7cdfc5b89bbb31d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "365347"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="bce4a-104">Сводное планирование для покрытия объекта и склада, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="bce4a-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce4a-105">В этом разделе описывается, как планируется номенклатура, которая имеет место и склад в качестве аналитики покрытия.</span><span class="sxs-lookup"><span data-stu-id="bce4a-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="bce4a-106">Аналитика склада обязательна.</span><span class="sxs-lookup"><span data-stu-id="bce4a-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="bce4a-107">Сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="bce4a-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="bce4a-108">Аналитика узла задана как обязательная и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="bce4a-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="bce4a-109">Аналитика склад является обязательной и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="bce4a-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="bce4a-110">Аналитики узла и склада заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="bce4a-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="bce4a-111">Другие аналитики также могут быть заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="bce4a-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="bce4a-112">Однако, они не подвержены влиянию многоузловых функций.</span><span class="sxs-lookup"><span data-stu-id="bce4a-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="bce4a-113">Следующий график иллюстрирует проведение сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="bce4a-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="bce4a-114">Параметры, упоминаемые на графике, и их местоположения приводятся ниже:</span><span class="sxs-lookup"><span data-stu-id="bce4a-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="bce4a-115">Для склада задано значение **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="bce4a-116">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="bce4a-117">На экспресс-вкладке **Сводное планирование** см. поле **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="bce4a-118">Покрытие номенклатуры определяется для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="bce4a-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="bce4a-119">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bce4a-120">Выберите номенклатуру, затем на панели операций на вкладке **План** щелкните **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="bce4a-121">Отношения пополнения определяются для склада.</span><span class="sxs-lookup"><span data-stu-id="bce4a-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="bce4a-122">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="bce4a-123">На экспресс-вкладке **Сводное планирование** см. группу поля **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="bce4a-124">Тип заказа по умолчанию задается как производство, заказу на покупку или канбан.</span><span class="sxs-lookup"><span data-stu-id="bce4a-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="bce4a-125">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bce4a-126">Выберите номенклатуру, затем на панели операций на вкладке **План** щелкните **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="bce4a-127">В форме **Параметры заказа по умолчанию** см. **Тип заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="bce4a-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Спрос для узла и покрытие склада, склад обязательный](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="bce4a-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bce4a-129">Additional resources</span></span>
--------

[<span data-ttu-id="bce4a-130">Сводное планирование и функция работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="bce4a-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="bce4a-131">Сводное планирование — покрытие объекта, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="bce4a-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bce4a-132">Сводное планирование — покрытие объекта, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="bce4a-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bce4a-133">Сводное планирование — покрытие объекта и склада, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="bce4a-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bce4a-134">Сводное планирование — Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="bce4a-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



