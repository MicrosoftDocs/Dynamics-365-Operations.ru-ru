---
title: Создание графика для сайта
description: В этой процедуре показано, как запланировать производственные заказы, которые еще не начаты для сайта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51c9ca8c402880f93a5998605d946b881d5ccdf5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835891"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="ee543-103">Создание графика для сайта</span><span class="sxs-lookup"><span data-stu-id="ee543-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee543-104">В этой процедуре показано, как запланировать производственные заказы, которые еще не начаты для сайта.</span><span class="sxs-lookup"><span data-stu-id="ee543-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="ee543-105">Для выполнения этой процедуры используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="ee543-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="ee543-106">Определение неначатых производственных заказов</span><span class="sxs-lookup"><span data-stu-id="ee543-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="ee543-107">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="ee543-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ee543-108">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="ee543-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ee543-109">Например, отфильтруйте поле "Сайт" по значению "1".</span><span class="sxs-lookup"><span data-stu-id="ee543-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="ee543-110">1 означает сайт в USMF.</span><span class="sxs-lookup"><span data-stu-id="ee543-110">1 represents a site in USMF.</span></span> <span data-ttu-id="ee543-111">Если вы не используете USMF, выберите сайт из собственной компании.</span><span class="sxs-lookup"><span data-stu-id="ee543-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="ee543-112">Откройте фильтра столбца "Статус".</span><span class="sxs-lookup"><span data-stu-id="ee543-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="ee543-113">Примените фильтр в поле "Статус" со значением "Запланировано", используя оператор фильтра "совпадает с".</span><span class="sxs-lookup"><span data-stu-id="ee543-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="ee543-114">Создание графика</span><span class="sxs-lookup"><span data-stu-id="ee543-114">Create a schedule</span></span>
1. <span data-ttu-id="ee543-115">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="ee543-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="ee543-116">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="ee543-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="ee543-117">Щелкните "Планирование заданий".</span><span class="sxs-lookup"><span data-stu-id="ee543-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="ee543-118">В поле "Направление планирования" выберите "Назад от даты поставки".</span><span class="sxs-lookup"><span data-stu-id="ee543-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="ee543-119">Выберите значение "Нет" в поле "Ограничение по мощности".</span><span class="sxs-lookup"><span data-stu-id="ee543-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="ee543-120">Выберите значение "Нет" в поле "Ограничение по материалам".</span><span class="sxs-lookup"><span data-stu-id="ee543-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="ee543-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ee543-121">Click OK.</span></span>
    * <span data-ttu-id="ee543-122">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="ee543-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="ee543-123">Просмотр результата спланированных производственных заказов</span><span class="sxs-lookup"><span data-stu-id="ee543-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="ee543-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ee543-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ee543-125">Можно пометить любую строку.</span><span class="sxs-lookup"><span data-stu-id="ee543-125">You can mark any row.</span></span>  
2. <span data-ttu-id="ee543-126">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="ee543-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="ee543-127">Щелкните "Все задания".</span><span class="sxs-lookup"><span data-stu-id="ee543-127">Click All jobs.</span></span>
    * <span data-ttu-id="ee543-128">На этой странице можно просмотреть список заданий.</span><span class="sxs-lookup"><span data-stu-id="ee543-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="ee543-129">На вкладке "Планирование" можно просмотреть дату начала и окончания задания.</span><span class="sxs-lookup"><span data-stu-id="ee543-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="ee543-130">Щелкните "Материалы".</span><span class="sxs-lookup"><span data-stu-id="ee543-130">Click Materials.</span></span>
    * <span data-ttu-id="ee543-131">На этой странице можно просмотреть расчетное потребление материала для операций по производственному заказу и доступные в данный момент запасы.</span><span class="sxs-lookup"><span data-stu-id="ee543-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

