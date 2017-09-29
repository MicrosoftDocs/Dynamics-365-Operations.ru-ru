---
title: "Использование трассировки для развертывания"
description: "Эта статья описывает, как можно использовать трассировку, чтобы исследовать причины результата развертывания заказа."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4e7f765f31ba34481cca78155e77eca61b106d50
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="709af-103">Использование трассировки для развертывания</span><span class="sxs-lookup"><span data-stu-id="709af-103">Use tracing for explosion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="709af-104">Эта статья описывает, как можно использовать трассировку, чтобы исследовать причины результата развертывания заказа.</span><span class="sxs-lookup"><span data-stu-id="709af-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="709af-105">Включив трассировку, вы можете просматривать информацию о факторах, которые участвуют в результатах развертывания определенного заказа.</span><span class="sxs-lookup"><span data-stu-id="709af-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="709af-106">Ниже приведены примеры, как можно использовать сведения трассировки:</span><span class="sxs-lookup"><span data-stu-id="709af-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="709af-107">Просмотр связей между действиями по запланированным заказам для оптимизации цепочки поставок и резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="709af-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="709af-108">Просмотр связей с заказами, которые уже утверждены.</span><span class="sxs-lookup"><span data-stu-id="709af-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="709af-109">Вы можете сосредоточиться на автоматическом подтверждении производных потребностей и более точной поставной приоритетов заказов.</span><span class="sxs-lookup"><span data-stu-id="709af-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="709af-110">Моделирование результатов планирования, чтобы определить, оптимальны ли параметры планирования.</span><span class="sxs-lookup"><span data-stu-id="709af-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="709af-111">Выявление того, как определяется информация, такая как даты производство, количества и приоритеты для заказов.</span><span class="sxs-lookup"><span data-stu-id="709af-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="709af-112">Вы можете просматривать информацию о фьючерсах и действия для выбранного заказа.</span><span class="sxs-lookup"><span data-stu-id="709af-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="709af-113">На странице **Развертывание** отслеживание информации доступно на вкладке **Объяснение** в верхней области.</span><span class="sxs-lookup"><span data-stu-id="709af-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="709af-114">Трассировка происходит при развертывании заказа.</span><span class="sxs-lookup"><span data-stu-id="709af-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="709af-115">Чтобы начать трассировку для заказа щелкните **Обновить**, а затем установите флажок **Включить трассировку**.</span><span class="sxs-lookup"><span data-stu-id="709af-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="709af-116">Можно использовать поле **Найти текст** для поиска конкретной информации в журнале.</span><span class="sxs-lookup"><span data-stu-id="709af-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="709af-117">Результаты поиска будут выделены в дереве.</span><span class="sxs-lookup"><span data-stu-id="709af-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="709af-118">См. также</span><span class="sxs-lookup"><span data-stu-id="709af-118">See also</span></span>
--------

[<span data-ttu-id="709af-119">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="709af-119">Master plans</span></span>](master-plans.md)




