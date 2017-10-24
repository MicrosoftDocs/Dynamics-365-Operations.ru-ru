--- 
title: "Планирование загрузок и отгрузок с помощью рабочего места планирования загрузки"
description: "В этой процедуре показано, как использовать рабочее место планирования загрузки для создания загрузки для заказа на продажу."
author: BibiSp
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
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="203ec-103">Планирование загрузок и отгрузок с помощью рабочего места планирования загрузки</span><span class="sxs-lookup"><span data-stu-id="203ec-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="203ec-104">В этой процедуре показано, как использовать рабочее место планирования загрузки для создания загрузки для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="203ec-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="203ec-105">Для начала необходимо будет создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="203ec-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="203ec-106">Эта процедура является элементом повседневной работы координатора транспортировки.</span><span class="sxs-lookup"><span data-stu-id="203ec-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="203ec-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="203ec-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="203ec-108">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="203ec-108">Create a sales order</span></span>
1. <span data-ttu-id="203ec-109">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="203ec-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="203ec-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="203ec-110">Click New.</span></span>
3. <span data-ttu-id="203ec-111">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="203ec-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="203ec-112">Выберите счет US-004.</span><span class="sxs-lookup"><span data-stu-id="203ec-112">Select account US-004.</span></span>
5. <span data-ttu-id="203ec-113">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="203ec-113">Click OK.</span></span>
6. <span data-ttu-id="203ec-114">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="203ec-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="203ec-115">Выберите номенклатуру A0001.</span><span class="sxs-lookup"><span data-stu-id="203ec-115">Select item A0001.</span></span>
    * <span data-ttu-id="203ec-116">A0001 поддерживает управление транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="203ec-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="203ec-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="203ec-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="203ec-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="203ec-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="203ec-119">В поле "Склад" введите "24".</span><span class="sxs-lookup"><span data-stu-id="203ec-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="203ec-120">В этом примере выберите склад 24.</span><span class="sxs-lookup"><span data-stu-id="203ec-120">In this example select warehouse 24.</span></span> <span data-ttu-id="203ec-121">Этот склад поддерживает управление транспортировкой и комплексные функции управления складом.</span><span class="sxs-lookup"><span data-stu-id="203ec-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="203ec-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="203ec-122">Click Save.</span></span>
12. <span data-ttu-id="203ec-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="203ec-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="203ec-124">Создание новой загрузки</span><span class="sxs-lookup"><span data-stu-id="203ec-124">Create a new load</span></span>
1. <span data-ttu-id="203ec-125">Перейдите в раздел "Управление транспортировкой" > "Планирование" > "Рабочее место планирования загрузки".</span><span class="sxs-lookup"><span data-stu-id="203ec-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="203ec-126">Перейдите на вкладку "Строки продаж".</span><span class="sxs-lookup"><span data-stu-id="203ec-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="203ec-127">Теперь вам предстоит построить загрузку для только что созданного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="203ec-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="203ec-128">Загрузки можно строить на основе предложения и спроса по заказам на покупку, заказам на перемещение и заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="203ec-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="203ec-129">В области действий щелкните "Поставки и спрос".</span><span class="sxs-lookup"><span data-stu-id="203ec-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="203ec-130">Щелкните "Для новой загрузки".</span><span class="sxs-lookup"><span data-stu-id="203ec-130">Click To new load.</span></span>
5. <span data-ttu-id="203ec-131">В поле "Код шаблона загрузки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="203ec-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="203ec-132">Шаблон загрузки определяет максимальные измерения для веса и объема всей загрузки.</span><span class="sxs-lookup"><span data-stu-id="203ec-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="203ec-133">Например, шаблон загрузки может представлять размер контейнера или грузовика.</span><span class="sxs-lookup"><span data-stu-id="203ec-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="203ec-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="203ec-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="203ec-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="203ec-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="203ec-136">Оценка и маршрутизация загрузки</span><span class="sxs-lookup"><span data-stu-id="203ec-136">Rate and route the load</span></span>
1. <span data-ttu-id="203ec-137">Щелкните "Оценка и маршрутизация".</span><span class="sxs-lookup"><span data-stu-id="203ec-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="203ec-138">Щелкните "Рабочее место маршрута ставки".</span><span class="sxs-lookup"><span data-stu-id="203ec-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="203ec-139">Щелкните "Магазин ставок".</span><span class="sxs-lookup"><span data-stu-id="203ec-139">Click Rate shop.</span></span>
4. <span data-ttu-id="203ec-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="203ec-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="203ec-141">Щелкните "Назначить".</span><span class="sxs-lookup"><span data-stu-id="203ec-141">Click Assign.</span></span>
6. <span data-ttu-id="203ec-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="203ec-142">Close the page.</span></span>
7. <span data-ttu-id="203ec-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="203ec-143">Close the page.</span></span>


