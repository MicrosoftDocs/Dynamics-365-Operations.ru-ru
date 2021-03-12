---
title: Внутрихолдинговое планирование
description: В этой теме описывается внутрихолдинговое планирование и объясняется, как настроить внутрихолдинговое планирование с оптимизацией планирования в Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0958ebccba345aa13a95f1fdf03946546cbbb714
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983602"
---
# <a name="intercompany-planning"></a><span data-ttu-id="9771e-103">Внутрихолдинговое планирование</span><span class="sxs-lookup"><span data-stu-id="9771e-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9771e-104">Для некоторых организаций операции логистики зависят от других юридических лиц (компаний) в организации.</span><span class="sxs-lookup"><span data-stu-id="9771e-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="9771e-105">Эти операции обрабатываются с помощью внутрихолдинговых продаж и покупок, поскольку каждое юридическое лицо имеет отдельный план счетов.</span><span class="sxs-lookup"><span data-stu-id="9771e-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="9771e-106">В этой теме описывается внутрихолдинговое планирование и объясняется, как настроить внутрихолдинговое планирование с оптимизацией планирования в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9771e-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="9771e-107">В этой теме используются следующие важные внутрихолдинговые термины:</span><span class="sxs-lookup"><span data-stu-id="9771e-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="9771e-108">**Вышестоящая** — относительная ссылка в цепочке утверждения или поставок.</span><span class="sxs-lookup"><span data-stu-id="9771e-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="9771e-109">Она указывает на перемещение в направлении поставщика сырья.</span><span class="sxs-lookup"><span data-stu-id="9771e-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="9771e-110">**Нижестоящая** — относительная ссылка в цепочке утверждения или поставок.</span><span class="sxs-lookup"><span data-stu-id="9771e-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="9771e-111">Она указывает на перемещение в направлении клиента.</span><span class="sxs-lookup"><span data-stu-id="9771e-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="9771e-112">**Спланированный внутрихолдинговый спрос** — запланированный спрос на продукт в компании на основе запланированного спроса на продукт из нижестоящей компании.</span><span class="sxs-lookup"><span data-stu-id="9771e-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="9771e-113">В сводном планировании план в одной компании может включать в себя запланированный внутрихолдинговый спрос, который относится к спланированным заказам из плана в другой компании.</span><span class="sxs-lookup"><span data-stu-id="9771e-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="9771e-114">Эта возможность полезна, поскольку она обеспечивает полную видимость спланированных заказов по компаниям.</span><span class="sxs-lookup"><span data-stu-id="9771e-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="9771e-115">Это также гарантирует, что все необходимые спланированные заказы на поставку созданы, но не требуется, чтобы спланированные заказы были утверждены для внутрихолдингового спроса.</span><span class="sxs-lookup"><span data-stu-id="9771e-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="9771e-116">Если сводное планирование выполняется из сводного плана, включающего запланированный нисходящий спрос, спланированные заказы на покупку от соответствующих внутрихолдинговых поставщиков будут включены в план как спрос.</span><span class="sxs-lookup"><span data-stu-id="9771e-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="9771e-117">Требуемая настройка</span><span class="sxs-lookup"><span data-stu-id="9771e-117">Required setup</span></span>

<span data-ttu-id="9771e-118">Чтобы использовать внутрихолдинговое планирование, необходимо подготовить систему следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9771e-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="9771e-119">Соответствующие продукты должны быть выпущены во всех соответствующих компаниях.</span><span class="sxs-lookup"><span data-stu-id="9771e-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="9771e-120">Дополнительные сведения см. в разделе [Настройка и использование внутрихолдинговой торговли в Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) в Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="9771e-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="9771e-121">Нисходящий спрос должен покрываться покупками от поставщика, у которого есть внутрихолдинговая связь с вышестоящей компанией и соответствующие складские аналитики по умолчанию (сайт и склад) для клиента.</span><span class="sxs-lookup"><span data-stu-id="9771e-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="9771e-122">Дополнительные сведения см. в разделе [Настройка и использование внутрихолдинговой торговли в Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) в Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="9771e-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="9771e-123">Сводный план в вышестоящей компании должен включать запланированный нисходящий спрос, а соответствующая компания и сводный план должны быть указаны в нижестоящих планах.</span><span class="sxs-lookup"><span data-stu-id="9771e-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="9771e-124">Включить спланированный нижестоящий спрос</span><span class="sxs-lookup"><span data-stu-id="9771e-124">Include planned downstream demand</span></span>

<span data-ttu-id="9771e-125">Выполните следующие шаги, чтобы настроить сводный план так, чтобы он включал запланированный нисходящий спрос.</span><span class="sxs-lookup"><span data-stu-id="9771e-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="9771e-126">Выберите **Сводное планирование \> Настройка \> Планы \> Сводные планы**.</span><span class="sxs-lookup"><span data-stu-id="9771e-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="9771e-127">Выберите или создайте сводный план.</span><span class="sxs-lookup"><span data-stu-id="9771e-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="9771e-128">На экспресс-вкладке **Внутрихолдинговое планирование** настройте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="9771e-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="9771e-129">**Включить спланированный нижестоящий спрос** — установите этот параметр на *Да*, чтобы включить внутрихолдинговое планирование для сводного плана.</span><span class="sxs-lookup"><span data-stu-id="9771e-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="9771e-130">**Нисходящие планы** — если для параметра **Включить спланированный нижестоящий спрос** выбрано значение *Да*, используйте панель инструментов и сетку для добавления необходимых сводных планов из других компаний.</span><span class="sxs-lookup"><span data-stu-id="9771e-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="9771e-131">Фиксация между компаниями с помощью многоуровневых сведений об источниках потребности</span><span class="sxs-lookup"><span data-stu-id="9771e-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="9771e-132">В многоуровневой информации об источниках потребности можно просматривать информацию об источниках потребности в нескольких компаниях, чтобы увидеть начальный источник спроса, покрываемый поставками.</span><span class="sxs-lookup"><span data-stu-id="9771e-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="9771e-133">Для просмотра многоуровневой информации об источнике потребности выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9771e-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="9771e-134">Перейдите в раздел **Сводное планирование \> Сводное планирование \> Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="9771e-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="9771e-135">Выберите или откройте спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="9771e-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="9771e-136">В области действий на вкладке **Просмотр**, в группе **Требования** выберите **Многоуровневая информация об источниках потребности**.</span><span class="sxs-lookup"><span data-stu-id="9771e-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="9771e-137">Внутрихолдинговый пример, в котором участвуют две компании</span><span class="sxs-lookup"><span data-stu-id="9771e-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="9771e-138">В данном примере запланированный производственный заказ создается в компании USMF для покрытия заказа на продажу в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="9771e-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="9771e-139">В компании USMF прямой спрос является запланированным внутрихолдинговым спросом.</span><span class="sxs-lookup"><span data-stu-id="9771e-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="9771e-140">Для того чтобы это требование отображалось в компании USMF, сводное планирование выпускается первым в DEMF, а затем в USMF.</span><span class="sxs-lookup"><span data-stu-id="9771e-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="9771e-141">На следующем рисунке показано, как этот пример может отображаться на странице **Многоуровневая информация об источниках потребности** для спланированного производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="9771e-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Внутрихолдинговый пример, в котором участвуют две компании](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="9771e-143">Внутрихолдинговый пример, в котором участвуют три компании</span><span class="sxs-lookup"><span data-stu-id="9771e-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="9771e-144">В данном примере запланированный заказ на покупку создается в компании USMF для покрытия заказа на продажу в компании FRRT.</span><span class="sxs-lookup"><span data-stu-id="9771e-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="9771e-145">В компаниях DEMF и USMF прямой спрос является запланированным внутрихолдинговым спросом.</span><span class="sxs-lookup"><span data-stu-id="9771e-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="9771e-146">Для того чтобы это требование отображалось в компании USMF, сводное планирование выпускается первым в FRRT, затем в DEMF и, наконец, в USMF.</span><span class="sxs-lookup"><span data-stu-id="9771e-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="9771e-147">На следующем рисунке показано, как этот пример может отображаться на странице **Многоуровневая информация об источниках потребности** для спланированного производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="9771e-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Внутрихолдинговый пример, в котором участвуют три компании](media/IntercompanyPlanning2.png)
