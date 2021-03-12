---
title: Завершение производственного заказа
description: Следующая процедура используется для завершения производственного заказа.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977821"
---
# <a name="end-a-production-order"></a><span data-ttu-id="a9bd1-103">Завершение производственного заказа</span><span class="sxs-lookup"><span data-stu-id="a9bd1-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9bd1-104">Следующая процедура используется для завершения производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="a9bd1-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a9bd1-106">Это последняя из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="a9bd1-107">Завершение производственного заказа</span><span class="sxs-lookup"><span data-stu-id="a9bd1-107">End a production order</span></span>
1. <span data-ttu-id="a9bd1-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="a9bd1-109">Выберите производственный заказ со статусом "Принятые".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="a9bd1-110">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="a9bd1-111">Щелкните "Готово".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-111">Click End.</span></span>
    * <span data-ttu-id="a9bd1-112">На этой странице можно подтвердить завершение производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="a9bd1-113">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-113">Click the General tab.</span></span>
5. <span data-ttu-id="a9bd1-114">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="a9bd1-115">В поле "Метод отходов" выберите "Распределение".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="a9bd1-116">При выборе метода распределения стоимость сданных в отходы материалов добавляется к готовым товарам.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="a9bd1-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="a9bd1-118">Проверка результатов расчета</span><span class="sxs-lookup"><span data-stu-id="a9bd1-118">Validate calculation results</span></span>
1. <span data-ttu-id="a9bd1-119">В области действий щелкните "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="a9bd1-120">Щелкните "Просмотр сравнения стоимости".</span><span class="sxs-lookup"><span data-stu-id="a9bd1-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="a9bd1-121">После завершения производственного заказа можно сравнить расчетную себестоимость и фактическую себестоимость для получения сведений о производственных различиях.</span><span class="sxs-lookup"><span data-stu-id="a9bd1-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
