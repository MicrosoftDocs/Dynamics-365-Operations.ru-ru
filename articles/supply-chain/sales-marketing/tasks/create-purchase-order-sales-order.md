---
title: Создание заказа на покупку из заказа на продажу
description: Эта процедура описывает создание заказа на покупку на основе заказа на продажу.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843393"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="4dd43-103">Создание заказа на покупку из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="4dd43-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dd43-104">Эта процедура описывает создание заказа на покупку на основе заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="4dd43-105">Количества продукта по заказу на покупку предназначены для удовлетворения спроса исходного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="4dd43-106">Выполнение спрос на продажу таким способ является альтернативой более всестороннему и оптимизированному методу планирование требований к распределению.</span><span class="sxs-lookup"><span data-stu-id="4dd43-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="4dd43-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="4dd43-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="4dd43-108">Создание заказа на покупку из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="4dd43-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="4dd43-109">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="4dd43-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="4dd43-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4dd43-110">Click New.</span></span>
3. <span data-ttu-id="4dd43-111">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4dd43-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4dd43-112">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4dd43-113">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="4dd43-113">Click OK.</span></span>
6. <span data-ttu-id="4dd43-114">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4dd43-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4dd43-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4dd43-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4dd43-116">При использовании USMF можно выбрать D0001.</span><span class="sxs-lookup"><span data-stu-id="4dd43-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="4dd43-117">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="4dd43-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="4dd43-118">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="4dd43-118">Click Add line.</span></span>
10. <span data-ttu-id="4dd43-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4dd43-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4dd43-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4dd43-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4dd43-121">При использовании USMF можно выбрать T0020.</span><span class="sxs-lookup"><span data-stu-id="4dd43-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="4dd43-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4dd43-123">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="4dd43-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="4dd43-124">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="4dd43-124">Click Save.</span></span>
15. <span data-ttu-id="4dd43-125">В области действий щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="4dd43-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="4dd43-126">Щелкните "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="4dd43-126">Click Purchase order.</span></span>
    * <span data-ttu-id="4dd43-127">На странице "Создание заказа на покупку" перечислены все открытые строки заказа на продажу, скопированные из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="4dd43-128">Можно просмотреть сведения о заказе и при необходимости можно изменять выбранные сведения, такие как количество по покупке и условия ценообразования, прежде чем вы создаете покупки.</span><span class="sxs-lookup"><span data-stu-id="4dd43-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="4dd43-129">Выберите параметр "Включить все".</span><span class="sxs-lookup"><span data-stu-id="4dd43-129">Select the Include all option.</span></span>
    * <span data-ttu-id="4dd43-130">Если требуется создать заказы на покупку только для подмножества строк заказа на продажу, установите это по отдельности.</span><span class="sxs-lookup"><span data-stu-id="4dd43-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="4dd43-131">В поле "Счет поставщика" уже может быть указан или не указан номер поставщика.</span><span class="sxs-lookup"><span data-stu-id="4dd43-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="4dd43-132">Если поставщик по умолчанию настроен для продукта (в соответствующем покрытии номенклатуры), то этот поставщик будет скопирован в строку.</span><span class="sxs-lookup"><span data-stu-id="4dd43-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="4dd43-133">В противном случае следует указать поставщика вручную.</span><span class="sxs-lookup"><span data-stu-id="4dd43-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="4dd43-134">В этом руководстве, независимо от того, содержит ли счет поставщика значение или нет, на следующих этапах описана процедура выбора нового поставщика, который отличается для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="4dd43-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="4dd43-135">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4dd43-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="4dd43-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="4dd43-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="4dd43-138">Выберите вторую строку заказа.</span><span class="sxs-lookup"><span data-stu-id="4dd43-138">Select the second order line.</span></span>
22. <span data-ttu-id="4dd43-139">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4dd43-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="4dd43-140">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="4dd43-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4dd43-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="4dd43-142">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="4dd43-142">Click Validate.</span></span>
26. <span data-ttu-id="4dd43-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4dd43-143">Click OK.</span></span>
    * <span data-ttu-id="4dd43-144">Сообщение указывает, что создан один или несколько заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="4dd43-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="4dd43-145">Система создает отдельный заказ на покупку для каждого поставщика, указанного для строк заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="4dd43-146">Это означает, что если несколько строк заказа на покупку должны поставляться одним и тем же поставщиком, будет создан один заказ на покупку с несколькими строками.</span><span class="sxs-lookup"><span data-stu-id="4dd43-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="4dd43-147">Просмотр заказов на покупку, созданных из заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="4dd43-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="4dd43-148">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="4dd43-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="4dd43-149">Щелкните "Связанные заказы".</span><span class="sxs-lookup"><span data-stu-id="4dd43-149">Click Related orders.</span></span>
    * <span data-ttu-id="4dd43-150">На странице "Связанные заказы" перечислены все заказы, созданные из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="4dd43-151">В этом примере имеется два заказа на покупку, созданные для двух разных поставщиков соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4dd43-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="4dd43-152">Щелкните для перехода по ссылке в поле "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="4dd43-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="4dd43-153">Каждая строка заказа на покупку ассоциируется со строкой заказа на продажу, из-за которой потребовалась покупка.</span><span class="sxs-lookup"><span data-stu-id="4dd43-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="4dd43-154">Связь с заказом на продажу отображается на вкладке "Продукта" на экспресс-вкладке "Сведения о строке" в полях "Тип ссылки", "Номер ссылки" и "Ссылка на лот".</span><span class="sxs-lookup"><span data-stu-id="4dd43-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="4dd43-155">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="4dd43-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="4dd43-156">Перейдите на вкладку "Продукт".</span><span class="sxs-lookup"><span data-stu-id="4dd43-156">Click the Product tab.</span></span>
    * <span data-ttu-id="4dd43-157">Ссылка на лот позволяет обеспечить отнесение затрат по данной покупке на присоединенный заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="4dd43-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="4dd43-158">Можно перейти к исходному заказу на продажу, открыв ссылку в поле "Номер ссылки".</span><span class="sxs-lookup"><span data-stu-id="4dd43-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

