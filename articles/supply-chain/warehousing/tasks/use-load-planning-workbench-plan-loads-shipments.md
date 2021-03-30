---
title: Планирование загрузок и отгрузок с помощью рабочего места планирования загрузки
description: В этом разделе показано, как использовать рабочее место планирования загрузки для создания загрузки для заказа на продажу.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 277b91944d8f7ee79bed9b85ee6ebd275e72c75b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223298"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="b0b69-103">Планирование загрузок и отгрузок с помощью рабочего места планирования загрузки</span><span class="sxs-lookup"><span data-stu-id="b0b69-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0b69-104">В этом разделе показано, как использовать рабочее место планирования загрузки для создания загрузки для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="b0b69-105">Для начала необходимо будет создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="b0b69-106">Эта процедура является элементом повседневной работы координатора транспортировки.</span><span class="sxs-lookup"><span data-stu-id="b0b69-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="b0b69-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b0b69-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="b0b69-108">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="b0b69-108">Create a sales order</span></span>
1. <span data-ttu-id="b0b69-109">Перейдите к **Область перехода > Модули > Расчеты с клиентами > Заказы > Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="b0b69-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-110">Select **New**.</span></span>
3. <span data-ttu-id="b0b69-111">В поле **Счет клиента** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="b0b69-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b0b69-112">Выберите счет **US-004**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="b0b69-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-113">Select **OK**.</span></span>
6. <span data-ttu-id="b0b69-114">В поле **Код номенклатуры** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="b0b69-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b0b69-115">Выбор номенклатуры **A0001**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-115">Select item **A0001**.</span></span> <span data-ttu-id="b0b69-116">**A0001** поддерживает управление транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="b0b69-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="b0b69-117">В поле **Сайт** выберите кнопку раскрывающегося списка, чтобы открыть поиск, затем выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b0b69-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="b0b69-118">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="b0b69-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="b0b69-119">В поле **Склад** введите «24» для этого примера.</span><span class="sxs-lookup"><span data-stu-id="b0b69-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="b0b69-120">Этот склад поддерживает управление транспортировкой и комплексные функции управления складом.</span><span class="sxs-lookup"><span data-stu-id="b0b69-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="b0b69-121">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-121">Select **Save**.</span></span>
12. <span data-ttu-id="b0b69-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="b0b69-123">Создание новой загрузки</span><span class="sxs-lookup"><span data-stu-id="b0b69-123">Create a new load</span></span>
1. <span data-ttu-id="b0b69-124">Перейдите в раздел **Область перехода > Модули > Управление транспортировкой > Планирование > Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="b0b69-125">Выберите вкладку **Строки продаж**. Теперь вам предстоит построить загрузку для только что созданного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="b0b69-126">Загрузки можно строить на основе предложения и спроса по заказам на покупку, заказам на перемещение и заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="b0b69-127">На панели операций выберите **Поставки и спрос**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="b0b69-128">Выберите **В новую загрузку**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-128">Select **To new load**.</span></span>
5. <span data-ttu-id="b0b69-129">В поле **Код шаблона загрузки** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b0b69-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="b0b69-130">Шаблон загрузки определяет максимальные измерения для веса и объема всей загрузки.</span><span class="sxs-lookup"><span data-stu-id="b0b69-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="b0b69-131">Например, шаблон загрузки может представлять размер контейнера или грузовика.</span><span class="sxs-lookup"><span data-stu-id="b0b69-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="b0b69-132">Выберите элемент номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b0b69-132">Select an item.</span></span>
6. <span data-ttu-id="b0b69-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="b0b69-134">Оценка и маршрутизация загрузки</span><span class="sxs-lookup"><span data-stu-id="b0b69-134">Rate and route the load</span></span>
1. <span data-ttu-id="b0b69-135">Выберите **Рейтинг и маршрутизация**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="b0b69-136">Выберите **Рабочее место маршрута ставки**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="b0b69-137">Выберите **Магазин ставок**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="b0b69-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b0b69-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b0b69-139">Выберите **Назначить**.</span><span class="sxs-lookup"><span data-stu-id="b0b69-139">Select **Assign**.</span></span>
6. <span data-ttu-id="b0b69-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b0b69-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]