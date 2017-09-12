--- 
title: "Регистрация поступления товаров по заказу на покупку"
description: "В этой процедуре показано, как зарегистрировать поступление товаров непосредственно в заказе на покупку."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="647ea-103">Регистрация поступления товаров по заказу на покупку</span><span class="sxs-lookup"><span data-stu-id="647ea-103">Record the receipt of goods on the purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="647ea-104">В этой процедуре показано, как зарегистрировать поступление товаров непосредственно в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="647ea-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="647ea-105">Также можно зарегистрировать поступление продуктов на складе, а затем зарегистрировать его в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="647ea-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="647ea-106">Эта задача обычно выполняется специалистом по закупке или координатором расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="647ea-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="647ea-107">Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="647ea-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="647ea-108">Этот пример описывает шаги создания простого заказа на покупку, чтобы можно процедуру можно было воспроизвести как руководство по задаче.</span><span class="sxs-lookup"><span data-stu-id="647ea-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="647ea-109">Если вы используете собственные данные в процедуре, вы начнете с подзадачи "Регистрация получения товаров".</span><span class="sxs-lookup"><span data-stu-id="647ea-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="647ea-110">Подготовка нового заказа на покупку для поступления товаров</span><span class="sxs-lookup"><span data-stu-id="647ea-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="647ea-111">Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="647ea-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="647ea-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="647ea-112">Click New.</span></span>
3. <span data-ttu-id="647ea-113">В поле "Счет поставщика" введите "US-101".</span><span class="sxs-lookup"><span data-stu-id="647ea-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="647ea-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="647ea-114">Click OK.</span></span>
5. <span data-ttu-id="647ea-115">В поле "Код номенклатуры" введите "M0001".</span><span class="sxs-lookup"><span data-stu-id="647ea-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="647ea-116">В поле "Количество" введите 5.</span><span class="sxs-lookup"><span data-stu-id="647ea-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="647ea-117">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="647ea-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="647ea-118">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="647ea-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="647ea-119">Регистрация получения товаров</span><span class="sxs-lookup"><span data-stu-id="647ea-119">Record receipt of goods</span></span>
1. <span data-ttu-id="647ea-120">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="647ea-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="647ea-121">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="647ea-121">Click Product receipt.</span></span>
    * <span data-ttu-id="647ea-122">Поле "Количество" позволяет выбрать различные параметры для количества, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="647ea-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="647ea-123">Например, если количество ранее было зарегистрировано на складе, можно выбрать параметр "Зарегистрированное количество".</span><span class="sxs-lookup"><span data-stu-id="647ea-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="647ea-124">В этом примере используется значение "Зарегистрированное количество".</span><span class="sxs-lookup"><span data-stu-id="647ea-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="647ea-125">В поле "Поступление продуктов" введите любое значение.</span><span class="sxs-lookup"><span data-stu-id="647ea-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="647ea-126">Это поле используется для ввода ссылки, которая будет использоваться как ваучер для журнала поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="647ea-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="647ea-127">Разверните раздел "Строки".</span><span class="sxs-lookup"><span data-stu-id="647ea-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="647ea-128">В поле "Количество" укажите "4".</span><span class="sxs-lookup"><span data-stu-id="647ea-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="647ea-129">Здесь можно вручную указать количество, которое получается по каждой строке в заказе.</span><span class="sxs-lookup"><span data-stu-id="647ea-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="647ea-130">Сверните раздел "Строки".</span><span class="sxs-lookup"><span data-stu-id="647ea-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="647ea-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="647ea-131">Click OK.</span></span>
    * <span data-ttu-id="647ea-132">Товары зарегистрированы как полученные по заказу на покупку, и журнал поступления продуктов был создан как документ, в котором это указано.</span><span class="sxs-lookup"><span data-stu-id="647ea-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="647ea-133">Можно использовать действие "Поступление продуктов" для просмотра журналов, созданных с заказом на покупку, чтобы узнать, что было получено и когда.</span><span class="sxs-lookup"><span data-stu-id="647ea-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


