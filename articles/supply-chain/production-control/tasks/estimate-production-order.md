--- 
title: "Оценка производственного заказа"
description: "Эту процедуру можно выполнять с помощью компании с демонстрационными данными USMF или применительно к собственным данным."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d34a891a5b655f801e46b8c07525cdcbc7a65c8
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="f88f7-103">Оценка производственного заказа</span><span class="sxs-lookup"><span data-stu-id="f88f7-103">Estimate a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f88f7-104">Эту процедуру можно выполнять с помощью компании с демонстрационными данными USMF или применительно к собственным данным.</span><span class="sxs-lookup"><span data-stu-id="f88f7-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="f88f7-105">В обоих случаях необходимо располагать открытым производственным заказом со статусом "Создано".</span><span class="sxs-lookup"><span data-stu-id="f88f7-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="f88f7-106">Это вторая из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="f88f7-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="f88f7-107">Оценка производственного заказа</span><span class="sxs-lookup"><span data-stu-id="f88f7-107">Estimate a production order</span></span>
1. <span data-ttu-id="f88f7-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="f88f7-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="f88f7-109">В сетке выберите заказ со статусом "Создано".</span><span class="sxs-lookup"><span data-stu-id="f88f7-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="f88f7-110">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="f88f7-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="f88f7-111">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="f88f7-111">Click Estimate.</span></span>
    * <span data-ttu-id="f88f7-112">На этом этапе рассчитывается оценочная стоимость одного производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="f88f7-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="f88f7-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f88f7-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="f88f7-114">Просмотр сведений расчета</span><span class="sxs-lookup"><span data-stu-id="f88f7-114">View the calculation details</span></span>
1. <span data-ttu-id="f88f7-115">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="f88f7-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="f88f7-116">Щелкните "Просмотреть сведения расчета".</span><span class="sxs-lookup"><span data-stu-id="f88f7-116">Click View calculation details.</span></span>
    * <span data-ttu-id="f88f7-117">На этой странице отображается детализация затрат.</span><span class="sxs-lookup"><span data-stu-id="f88f7-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="f88f7-118">Например, можно просматривать общую себестоимость на единицу измерения для готовой продукции в первой строке.</span><span class="sxs-lookup"><span data-stu-id="f88f7-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="f88f7-119">Последующие строки содержат стоимость согласно спецификации, маршруту производства и косвенным затратам.</span><span class="sxs-lookup"><span data-stu-id="f88f7-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  


