--- 
title: "Отгрузка заказов на продажу без складирования"
description: "Это руководство демонстрирует способ обновления заказа на продажу, когда продукты отгружены клиенту."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
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
ms.openlocfilehash: d0ad0869907b23ce5e0b44e3e9ecee3f2cd34ede
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="d4f77-103">Отгрузка заказов на продажу без складирования</span><span class="sxs-lookup"><span data-stu-id="d4f77-103">Ship sales orders without warehousing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4f77-104">Это руководство демонстрирует способ обновления заказа на продажу, когда продукты отгружены клиенту.</span><span class="sxs-lookup"><span data-stu-id="d4f77-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="d4f77-105">Руководство применимо к потоку выполнения, который не был настроен для управления складом (ни основное, ни расширенное управление складом), и поэтому не требует регистрации комплектации продукта перед отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="d4f77-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="d4f77-106">Эту процедуру можно выполнить со своими данными или с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="d4f77-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="d4f77-107">В обоих случаях перед началом этой задачи создайте заказ на продажу для инвентаризованного продукта с количеством более 1.</span><span class="sxs-lookup"><span data-stu-id="d4f77-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="d4f77-108">Чтобы избежать ошибок разноски, необходимо проверить, что количество продукта в наличии на сайте или складе, выбранном в заказе, охватывает количество по заказу.</span><span class="sxs-lookup"><span data-stu-id="d4f77-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="d4f77-109">Разнесение отборочной накладной для заказа</span><span class="sxs-lookup"><span data-stu-id="d4f77-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="d4f77-110">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="d4f77-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="d4f77-111">В списке найдите и выберите заказ, созданный для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="d4f77-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="d4f77-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d4f77-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d4f77-113">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="d4f77-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="d4f77-114">Щелкните "Разноска отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="d4f77-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="d4f77-115">Разверните или сверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="d4f77-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="d4f77-116">В поле "Количество" выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="d4f77-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="d4f77-117">Другие параметры включают "Немедленная поставка" и "Скомплектовано".</span><span class="sxs-lookup"><span data-stu-id="d4f77-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="d4f77-118">Если строка заказа должна отгружаться частично и поле "Немедленная поставка" в строке заказа содержит количество, необходимо выбрать "Немедленная поставка".</span><span class="sxs-lookup"><span data-stu-id="d4f77-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="d4f77-119">Если поток выполнения организации включает комплектацию как отдельный процесс, который управляется и зарегистрирован с листом подбора, необходимо выбрать "Скомплектовано".</span><span class="sxs-lookup"><span data-stu-id="d4f77-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="d4f77-120">Убедитесь, что параметр "Разноска" установлен как "Да".</span><span class="sxs-lookup"><span data-stu-id="d4f77-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="d4f77-121">Установите параметр "Печать отборочной накладной" в значение "Да".</span><span class="sxs-lookup"><span data-stu-id="d4f77-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="d4f77-122">На вкладке "Обзор" содержится список отборочных накладных, которые будут созданы в этой разноске.</span><span class="sxs-lookup"><span data-stu-id="d4f77-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="d4f77-123">Если вы отгружаете отдельный заказ, обычно будет одна отборочная накладная.</span><span class="sxs-lookup"><span data-stu-id="d4f77-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="d4f77-124">Однако если строки этого заказа были отгружены из разных сайтов, разноска будет автоматически разделена на соответствующее число документов.</span><span class="sxs-lookup"><span data-stu-id="d4f77-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="d4f77-125">Это необходимое условие, которое нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="d4f77-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="d4f77-126">Аналогичным образом, разноска также будет разбита на несколько документов, если строки заказа были отгружены по различным адресам доставки и политика отгрузки настроена на обязательное использование разделения.</span><span class="sxs-lookup"><span data-stu-id="d4f77-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="d4f77-127">На вкладке "Строки" выберите строку для отгружаемой строки заказа.</span><span class="sxs-lookup"><span data-stu-id="d4f77-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="d4f77-128">В поле "Обновить" введите число, меньше чем исходное количество.</span><span class="sxs-lookup"><span data-stu-id="d4f77-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="d4f77-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4f77-129">Click OK.</span></span>
12. <span data-ttu-id="d4f77-130">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="d4f77-130">Click Yes.</span></span>
13. <span data-ttu-id="d4f77-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4f77-131">Close the page.</span></span>
14. <span data-ttu-id="d4f77-132">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="d4f77-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="d4f77-133">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="d4f77-133">Click Change view.</span></span>
16. <span data-ttu-id="d4f77-134">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="d4f77-134">Click Header view.</span></span>
    * <span data-ttu-id="d4f77-135">Если все строки заказа полностью отгружены, статус заказа изменяется с открытого на доставленный.</span><span class="sxs-lookup"><span data-stu-id="d4f77-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="d4f77-136">В этом примере строка заказа была отгружена частично.</span><span class="sxs-lookup"><span data-stu-id="d4f77-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="d4f77-137">Поэтому статус заказа остается открытым.</span><span class="sxs-lookup"><span data-stu-id="d4f77-137">This is why the order status remains Open.</span></span>     
    * <span data-ttu-id="d4f77-138">Поле статуса документа задается как "Отборочная накладная", поскольку хотя бы одна строка заказа уже была отгружена.</span><span class="sxs-lookup"><span data-stu-id="d4f77-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="d4f77-139">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="d4f77-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="d4f77-140">Щелкните "Количество по строке".</span><span class="sxs-lookup"><span data-stu-id="d4f77-140">Click Line quantity.</span></span>
19. <span data-ttu-id="d4f77-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4f77-141">Close the page.</span></span>
20. <span data-ttu-id="d4f77-142">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="d4f77-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="d4f77-143">Щелкните "Отборочная накладная".</span><span class="sxs-lookup"><span data-stu-id="d4f77-143">Click Packing slip.</span></span>
    * <span data-ttu-id="d4f77-144">Страница "Журнал отборочных накладных" содержит все документы по отборочным накладным, созданным для вашего заказа.</span><span class="sxs-lookup"><span data-stu-id="d4f77-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="d4f77-145">Можно просмотреть сведения по каждому документу и распечатать их, если требуется.</span><span class="sxs-lookup"><span data-stu-id="d4f77-145">You can review details of each document and print them, if needed.</span></span>  


