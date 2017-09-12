---
title: "Сводное планирование для покрытия объекта, склад не является обязательным"
description: "В этом разделе описывается, как планируется номенклатура, которая имеет покрытие в качестве аналитики объекта."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 79582e92daeaf0afb032448d36be12edd0926089
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="7799d-103">Сводное планирование для покрытия объекта, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="7799d-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7799d-104">В этом разделе описывается, как планируется номенклатура, которая имеет покрытие в качестве аналитики объекта.</span><span class="sxs-lookup"><span data-stu-id="7799d-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="7799d-105">Сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="7799d-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="7799d-106">Аналитика узла задана как обязательная и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="7799d-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="7799d-107">Аналитика склада не задана как обязательная.</span><span class="sxs-lookup"><span data-stu-id="7799d-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="7799d-108">Склад может быть известен, но он не используется в расчете сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="7799d-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="7799d-109">Аналитика узла задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="7799d-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="7799d-110">Аналитика склада не задана для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="7799d-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="7799d-111">Поэтому поставки и спрос объединяются узлом и, возможно, другими аналитиками планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="7799d-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="7799d-112">Следующий график иллюстрирует проведение сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="7799d-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="7799d-113">Параметры, упоминаемые на графике, и их местоположения приводятся ниже:</span><span class="sxs-lookup"><span data-stu-id="7799d-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="7799d-114">Покрытие номенклатуры определяется для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="7799d-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="7799d-115">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="7799d-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="7799d-116">Выберите номенклатуру, затем щелкните **План &gt; Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="7799d-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="7799d-117">Отношения пополнения определяются для склада.</span><span class="sxs-lookup"><span data-stu-id="7799d-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="7799d-118">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="7799d-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="7799d-119">На вкладке **Сводное планирование** см. группу поля **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="7799d-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="7799d-120">Тип заказа по умолчанию задается как производство, заказу на покупку или канбан.</span><span class="sxs-lookup"><span data-stu-id="7799d-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="7799d-121">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="7799d-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="7799d-122">Выберите номенклатуру и после этого щелкните **План &gt; Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="7799d-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="7799d-123">В форме **Параметры заказа по умолчанию** см. поле **Тип заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="7799d-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Спрос для склада покрытия узла необязательный](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a><span data-ttu-id="7799d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7799d-125">See also</span></span>
--------

[<span data-ttu-id="7799d-126">Сводное планирование и функция работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="7799d-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="7799d-127">Сводное планирование — покрытие объекта, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="7799d-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="7799d-128">Сводное планирование — покрытие объекта и склада, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="7799d-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="7799d-129">Сводное планирование — покрытие объекта и склада, склад является обязательным</span><span class="sxs-lookup"><span data-stu-id="7799d-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="7799d-130">Сводное планирование — определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="7799d-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




