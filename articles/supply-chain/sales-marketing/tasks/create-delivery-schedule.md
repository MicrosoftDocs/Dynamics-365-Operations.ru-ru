--- 
title: "Создание графика поставки"
description: "В этой процедуре показано, как создать график поставки для заказа на продажу."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 13add634e275a0156c2c0f87d1fec80385d62fea
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="988f0-103">Создание графика поставки</span><span class="sxs-lookup"><span data-stu-id="988f0-103">Create a delivery schedule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="988f0-104">В этой процедуре показано, как создать график поставки для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="988f0-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="988f0-105">График поставки используется, когда количество в заказе или предложении должно быть поставлено в нескольких отгрузках.</span><span class="sxs-lookup"><span data-stu-id="988f0-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="988f0-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="988f0-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="988f0-107">Создание графика поставки</span><span class="sxs-lookup"><span data-stu-id="988f0-107">Create delivery schedule</span></span>
1. <span data-ttu-id="988f0-108">Перейдите в раздел "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="988f0-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="988f0-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="988f0-109">Click New.</span></span>
3. <span data-ttu-id="988f0-110">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="988f0-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="988f0-111">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="988f0-111">Click OK.</span></span>
5. <span data-ttu-id="988f0-112">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="988f0-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="988f0-113">В поле "Количество" введите число больше 1.</span><span class="sxs-lookup"><span data-stu-id="988f0-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="988f0-114">Щелкните "Строка заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="988f0-114">Click Sales order line.</span></span>
8. <span data-ttu-id="988f0-115">Щелкните "График поставки".</span><span class="sxs-lookup"><span data-stu-id="988f0-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="988f0-116">На странице "График поставки" можно указать число отгрузок, необходимых для того, чтобы поставить общее количество строки заказа клиенту.</span><span class="sxs-lookup"><span data-stu-id="988f0-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="988f0-117">По умолчанию система копирует общее количество и другие сведения поставки из первоначальной строки продажи в первую строку графика поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="988f0-118">В этом примере создадим график с двумя отгрузками, при этом дата второй отгрузки будет на неделю отстоять от даты первой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="988f0-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="988f0-119">В поле "Количество" введите число, которое составляет часть общего количества.</span><span class="sxs-lookup"><span data-stu-id="988f0-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="988f0-120">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="988f0-120">Click New.</span></span>
11. <span data-ttu-id="988f0-121">В поле "Количество" введите оставшееся количество.</span><span class="sxs-lookup"><span data-stu-id="988f0-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="988f0-122">В поле "Запрошенная дата отгрузки" введите дату, которая на одну неделю отстоит от даты в первой строке поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="988f0-123">Два параметра на экспресс-вкладке "Преобразование накладных расходов" определяют способ распределения накладных расходов по строкам графика поставки после их назначения исходной строке заказа.</span><span class="sxs-lookup"><span data-stu-id="988f0-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="988f0-124">Если выбрать параметр "Копировать валовые суммы", одна и та же сумма накладных расходов будет скопирована в каждую строку.</span><span class="sxs-lookup"><span data-stu-id="988f0-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="988f0-125">Если выбрать параметр "Назначить строкам поставки", накладные расходы будут в равной степени поделены между строками поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="988f0-126">Только постоянные расходы могут быть распределены, в то время как переменные расходы по-прежнему будут скопированы в строки.</span><span class="sxs-lookup"><span data-stu-id="988f0-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="988f0-127">Переместите указатель мыши со второй строки поставки, чтобы обновить страницу.</span><span class="sxs-lookup"><span data-stu-id="988f0-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="988f0-128">Можно отследить общее количество, распределенное по строкам графика поставки, просмотрев поля "Итого" и "Остаток".</span><span class="sxs-lookup"><span data-stu-id="988f0-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="988f0-129">Если оставшееся количество равно нулю, это значит, что все количество из исходной строки распределено в график.</span><span class="sxs-lookup"><span data-stu-id="988f0-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="988f0-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="988f0-130">Click OK.</span></span>
    * <span data-ttu-id="988f0-131">График поставки скопирован в строки заказа.</span><span class="sxs-lookup"><span data-stu-id="988f0-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="988f0-132">Исходная строка заказа, которая называется коммерческой строкой, преобразована в строку заказа с несколькими поставками.</span><span class="sxs-lookup"><span data-stu-id="988f0-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="988f0-133">Она отмечена отдельным значком и выступает в качестве заголовка для строк поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="988f0-134">Две новые строки, которые называются строками поставки, составляют единый график поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="988f0-135">Заказ будет обработан на основании этих строк, а не исходной строки.</span><span class="sxs-lookup"><span data-stu-id="988f0-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="988f0-136">При печати документов, таких как квитанции подтверждений, листы подбора, отборочные накладные или накладные, отображаются только строки поставки.</span><span class="sxs-lookup"><span data-stu-id="988f0-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="988f0-137">В строках поставки могут быть указаны различные даты, количества и способы поставки или аналитики хранения, такие как сайт и склад.</span><span class="sxs-lookup"><span data-stu-id="988f0-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="988f0-138">Однако аналитики продукта всегда должны соответствовать аналитикам в коммерческой строке и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="988f0-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="988f0-139">В поле "Количество" введите число больше текущего.</span><span class="sxs-lookup"><span data-stu-id="988f0-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="988f0-140">Выберите коммерческую строку, чтобы просмотреть результат пересчета количества.</span><span class="sxs-lookup"><span data-stu-id="988f0-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="988f0-141">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="988f0-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="988f0-142">Щелкните "Разноска отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="988f0-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="988f0-143">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="988f0-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="988f0-144">В поле "Количество" выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="988f0-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="988f0-145">Обратите внимание, что отборочная накладная будет создана для двух строк графика поставки, а не исходной строки заказа.</span><span class="sxs-lookup"><span data-stu-id="988f0-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="988f0-146">Выберите значение "Да" в поле "Печать отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="988f0-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="988f0-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="988f0-147">Click OK.</span></span>
23. <span data-ttu-id="988f0-148">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="988f0-148">Click Yes.</span></span>
24. <span data-ttu-id="988f0-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="988f0-149">Close the page.</span></span>


