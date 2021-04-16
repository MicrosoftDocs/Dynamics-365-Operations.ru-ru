---
title: Сводное планирование для покрытия объекта и склада, склад не является обязательным
description: В этом разделе описывается, как планируется номенклатура, которая имеет место и склад в качестве аналитики покрытия. Аналитика склада не обязательна.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8350646e70c7ea7d705a69ecb52f389e829a0fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833481"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="01a49-104">Сводное планирование для покрытия объекта и склада, склад не является обязательным</span><span class="sxs-lookup"><span data-stu-id="01a49-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01a49-105">В этом разделе описывается, как планируется номенклатура, которая имеет место и склад в качестве аналитики покрытия.</span><span class="sxs-lookup"><span data-stu-id="01a49-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="01a49-106">Аналитика склада не обязательна.</span><span class="sxs-lookup"><span data-stu-id="01a49-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="01a49-107">Сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="01a49-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="01a49-108">Аналитика узла задана как обязательная и должна быть введена для проводки по спросу.</span><span class="sxs-lookup"><span data-stu-id="01a49-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="01a49-109">Этот параметр нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="01a49-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="01a49-110">Аналитика склада не задана как обязательная.</span><span class="sxs-lookup"><span data-stu-id="01a49-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="01a49-111">Склад может быть известен, но он не используется в расчете сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="01a49-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="01a49-112">Аналитики узла и склада заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="01a49-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="01a49-113">Другие аналитики также могут быть заданы для планирования покрытия.</span><span class="sxs-lookup"><span data-stu-id="01a49-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="01a49-114">Однако, они не подвержены влиянию многоузловых функций.</span><span class="sxs-lookup"><span data-stu-id="01a49-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="01a49-115">Следующий график иллюстрирует проведение сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="01a49-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="01a49-116">Параметры, упоминаемые на графике, и их местоположения приводятся ниже:</span><span class="sxs-lookup"><span data-stu-id="01a49-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="01a49-117">Для склада задано значение "Вручную".</span><span class="sxs-lookup"><span data-stu-id="01a49-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="01a49-118">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="01a49-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="01a49-119">На экспресс-вкладке **Сводное планирование** см. поле **Вручную**.</span><span class="sxs-lookup"><span data-stu-id="01a49-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="01a49-120">Покрытие номенклатуры определяется для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="01a49-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="01a49-121">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="01a49-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="01a49-122">Выберите номенклатуру, затем на панели операций на вкладке **План** щелкните **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="01a49-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="01a49-123">Отношения пополнения определяются для склада.</span><span class="sxs-lookup"><span data-stu-id="01a49-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="01a49-124">Щелкните **Управление запасами &gt; Настройка &gt; Разделение запасов &gt; Склады**.</span><span class="sxs-lookup"><span data-stu-id="01a49-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="01a49-125">На экспресс-вкладке **Сводное планирование** см. группу поля **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="01a49-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="01a49-126">Тип заказа по умолчанию задается как производство, заказу на покупку или канбан.</span><span class="sxs-lookup"><span data-stu-id="01a49-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="01a49-127">Щелкните **Управление сведениями о продукте &gt; Продукты &gt; Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="01a49-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="01a49-128">Выберите номенклатуру, затем на панели операций на вкладке **План** щелкните **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="01a49-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="01a49-129">В форме **Параметры заказа по умолчанию** см. **Тип заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="01a49-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Спрос для узла и покрытие склада, склад необязательный](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="01a49-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01a49-131">Additional resources</span></span>
--------

[<span data-ttu-id="01a49-132">Обзор сводного планирования и функции работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="01a49-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="01a49-133">Сводное планирование для покрытия сайта, обязательный склад</span><span class="sxs-lookup"><span data-stu-id="01a49-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="01a49-134">Сводное планирование для покрытия сайта и склада, склад обязателен</span><span class="sxs-lookup"><span data-stu-id="01a49-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="01a49-135">Сводное планирование для покрытия сайта и склада, склад не обязателен</span><span class="sxs-lookup"><span data-stu-id="01a49-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="01a49-136">Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="01a49-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]