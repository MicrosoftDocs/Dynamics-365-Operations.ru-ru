--- 
title: "Управление удержаниями заказов"
description: "В этой процедуре показано, как заблокировать заказы на продажу клиента, как работать с извлеченными удержаниями заказов и как снять блокировку заказов."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9a520b2af7cdfef325f1fa96504f2a20078ed80
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="manage-order-holds"></a><span data-ttu-id="fafc2-103">Управление удержаниями заказов</span><span class="sxs-lookup"><span data-stu-id="fafc2-103">Manage order holds</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fafc2-104">В этой процедуре показано, как заблокировать заказы на продажу клиента, как работать с извлеченными удержаниями заказов и как снять блокировку заказов.</span><span class="sxs-lookup"><span data-stu-id="fafc2-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="fafc2-105">Заказ может быть заблокирован по разным причинам.</span><span class="sxs-lookup"><span data-stu-id="fafc2-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="fafc2-106">Например, заказ можно заблокировать, пока не будет проверен адрес или способ оплаты клиента или пока менеджер не проверит кредитный лимит клиента.</span><span class="sxs-lookup"><span data-stu-id="fafc2-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="fafc2-107">Пока заказ находится в заблокированном состоянии, его невозможно обрабатывать на складе для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="fafc2-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="fafc2-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="fafc2-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="fafc2-109">Настройка удержаний заказов</span><span class="sxs-lookup"><span data-stu-id="fafc2-109">Set up order holds</span></span>
1. <span data-ttu-id="fafc2-110">Перейдите в раздел "Продажи и маркетинг" > "Настройка" > "Заказы на продажу" > "Коды удержания заказов".</span><span class="sxs-lookup"><span data-stu-id="fafc2-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="fafc2-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fafc2-111">Click New.</span></span>
3. <span data-ttu-id="fafc2-112">В поле "Код удержания" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fafc2-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="fafc2-113">Например, введите "Перезвонить".</span><span class="sxs-lookup"><span data-stu-id="fafc2-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="fafc2-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fafc2-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fafc2-115">Например, удержание заказа в ожидании ответного вызова клиента.</span><span class="sxs-lookup"><span data-stu-id="fafc2-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="fafc2-116">При желании установите флажок "Удалить резервирования", чтобы удалить все физические резервирования из заказа при добавлении этого кода удержания.</span><span class="sxs-lookup"><span data-stu-id="fafc2-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="fafc2-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fafc2-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="fafc2-118">Блокировка заказа</span><span class="sxs-lookup"><span data-stu-id="fafc2-118">Place order on hold</span></span>
1. <span data-ttu-id="fafc2-119">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="fafc2-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="fafc2-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fafc2-120">Click New.</span></span>
3. <span data-ttu-id="fafc2-121">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fafc2-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="fafc2-122">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="fafc2-122">Click OK.</span></span>
5. <span data-ttu-id="fafc2-123">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fafc2-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="fafc2-124">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="fafc2-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="fafc2-125">В области действий щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="fafc2-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="fafc2-126">Нажмите кнопку "Удержания заказов".</span><span class="sxs-lookup"><span data-stu-id="fafc2-126">Click Order holds.</span></span>
9. <span data-ttu-id="fafc2-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fafc2-127">Click New.</span></span>
10. <span data-ttu-id="fafc2-128">В поле "Код удержания" выберите код, который вы создали в предыдущей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="fafc2-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="fafc2-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fafc2-129">Click Save.</span></span>
12. <span data-ttu-id="fafc2-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fafc2-130">Close the page.</span></span>
13. <span data-ttu-id="fafc2-131">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="fafc2-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="fafc2-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fafc2-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fafc2-133">В заказах, которые в данный момент заблокированы, поля "Не обрабатывать" и "Заблокировано" помечены.</span><span class="sxs-lookup"><span data-stu-id="fafc2-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="fafc2-134">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="fafc2-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="fafc2-135">Управление удержаниями заказов</span><span class="sxs-lookup"><span data-stu-id="fafc2-135">Manage order holds</span></span>
1. <span data-ttu-id="fafc2-136">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Открытые заказы" > "Удержания заказов".</span><span class="sxs-lookup"><span data-stu-id="fafc2-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="fafc2-137">Страница удержаний заказов выступает в роли рабочего места, где можно получить обзор всех текущих и обработанных удержаний, а также обработать их и связанные заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="fafc2-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="fafc2-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="fafc2-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="fafc2-139">В области действий щелкните "Заблокировать оформление".</span><span class="sxs-lookup"><span data-stu-id="fafc2-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="fafc2-140">Щелкните "Извлечь".</span><span class="sxs-lookup"><span data-stu-id="fafc2-140">Click Check out.</span></span>
5. <span data-ttu-id="fafc2-141">В списке снимите пометку выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="fafc2-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="fafc2-142">В поле "Оформление заказа" теперь отображается ваш идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="fafc2-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="fafc2-143">Щелкните "Сбросить извлечение".</span><span class="sxs-lookup"><span data-stu-id="fafc2-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="fafc2-144">В области действий щелкните "Снять блокировку".</span><span class="sxs-lookup"><span data-stu-id="fafc2-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="fafc2-145">Когда вы будете готовы снять блокировку и разрешить переход заказа к следующему шагу выполнения, снимите удержание.</span><span class="sxs-lookup"><span data-stu-id="fafc2-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="fafc2-146">Если заказ не требует изменений, можно выполнить действие "Снять удержания".</span><span class="sxs-lookup"><span data-stu-id="fafc2-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="fafc2-147">Однако можно использовать действие "Очистить и изменить", если при снятии блокировки заказ должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="fafc2-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="fafc2-148">Действие "Очистить и отправить" применяется только при использовании функции центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="fafc2-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="fafc2-149">Нажмите кнопку "Снять удержания".</span><span class="sxs-lookup"><span data-stu-id="fafc2-149">Click Clear holds.</span></span>
    * <span data-ttu-id="fafc2-150">Удержание теперь снято из заказа и удалено из списка активных удержаний.</span><span class="sxs-lookup"><span data-stu-id="fafc2-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="fafc2-151">Для просмотра всех удержаний или их подмножества в соответствии с конкретным статусом измените значение в поле "Показать".</span><span class="sxs-lookup"><span data-stu-id="fafc2-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     


