--- 
title: "Завершение производственного заказа"
description: "Следующая процедура используется для завершения производственного заказа."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="end-a-production-order"></a><span data-ttu-id="91287-103">Завершение производственного заказа</span><span class="sxs-lookup"><span data-stu-id="91287-103">End a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91287-104">Следующая процедура используется для завершения производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="91287-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="91287-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="91287-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91287-106">Это последняя из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="91287-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="91287-107">Завершение производственного заказа</span><span class="sxs-lookup"><span data-stu-id="91287-107">End a production order</span></span>
1. <span data-ttu-id="91287-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="91287-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="91287-109">Выберите производственный заказ со статусом "Принятые".</span><span class="sxs-lookup"><span data-stu-id="91287-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="91287-110">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="91287-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="91287-111">Щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="91287-111">Click End.</span></span>
    * <span data-ttu-id="91287-112">На этой странице можно подтвердить завершение производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="91287-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="91287-113">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="91287-113">Click the General tab.</span></span>
5. <span data-ttu-id="91287-114">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="91287-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="91287-115">В поле "Метод отходов" выберите "Распределение".</span><span class="sxs-lookup"><span data-stu-id="91287-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="91287-116">При выборе метода распределения стоимость сданных в отходы материалов добавляется к готовым товарам.</span><span class="sxs-lookup"><span data-stu-id="91287-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="91287-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91287-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="91287-118">Проверка результатов расчета</span><span class="sxs-lookup"><span data-stu-id="91287-118">Validate calculation results</span></span>
1. <span data-ttu-id="91287-119">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="91287-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="91287-120">Щелкните "Просмотр сравнения стоимости".</span><span class="sxs-lookup"><span data-stu-id="91287-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="91287-121">После завершения производственного заказа можно сравнить расчетную себестоимость и фактическую себестоимость для получения сведений о производственных различиях.</span><span class="sxs-lookup"><span data-stu-id="91287-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


