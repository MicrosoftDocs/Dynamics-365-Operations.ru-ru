---
title: Создание плана для сайта
description: Планировщик производства рассчитывает потребности в материалах и потребности в мощностях для производства конкретной номенклатуры.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560332"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="8a755-103">Создание плана для сайта</span><span class="sxs-lookup"><span data-stu-id="8a755-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a755-104">Планировщик производства рассчитывает потребности в материалах и потребности в мощностях для производства конкретной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8a755-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="8a755-105">После создания исходных предложений он обнаруживает заказы на сайте, для которого он планирует и утверждает заказы, начиная со срочных.</span><span class="sxs-lookup"><span data-stu-id="8a755-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="8a755-106">Самые срочные заказы — это заказы, которые необходимо утвердить на текущую дату.</span><span class="sxs-lookup"><span data-stu-id="8a755-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="8a755-107">Для выполнения этих задач используйте компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="8a755-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="8a755-108">Создание плана материально-технического обеспечения и мощностей для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="8a755-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="8a755-109">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="8a755-109">Click Master planning.</span></span>
    * <span data-ttu-id="8a755-110">Необходимо перейти к панели мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a755-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="8a755-111">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="8a755-111">Click Run.</span></span>
3. <span data-ttu-id="8a755-112">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="8a755-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="8a755-113">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="8a755-113">Click Filter.</span></span>
5. <span data-ttu-id="8a755-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8a755-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8a755-115">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a755-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8a755-116">Пример: D0001</span><span class="sxs-lookup"><span data-stu-id="8a755-116">Example: D0001</span></span>  
7. <span data-ttu-id="8a755-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a755-117">Click OK.</span></span>
8. <span data-ttu-id="8a755-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a755-118">Click OK.</span></span>
    * <span data-ttu-id="8a755-119">Это может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="8a755-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="8a755-120">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="8a755-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="8a755-121">Определение срочных спланированных заказов для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="8a755-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="8a755-122">Откройте фильтр столбца "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="8a755-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="8a755-123">Примените фильтр к полю "Код номенклатуры" со значением "D0001", используя оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="8a755-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="8a755-124">Откройте фильтр столбца "Дата заказа".</span><span class="sxs-lookup"><span data-stu-id="8a755-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="8a755-125">Примените фильтр в поле "Дата заказа" со значением текущей даты, используя оператор фильтра "совпадает с".</span><span class="sxs-lookup"><span data-stu-id="8a755-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="8a755-126">Утверждение срочных заказов для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="8a755-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="8a755-127">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="8a755-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="8a755-128">Щелкните "Утверждение".</span><span class="sxs-lookup"><span data-stu-id="8a755-128">Click Firm.</span></span>
3. <span data-ttu-id="8a755-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a755-129">Click OK.</span></span>

