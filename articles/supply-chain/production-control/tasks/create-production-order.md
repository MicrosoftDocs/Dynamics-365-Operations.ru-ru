--- 
title: "Создание производственного заказа"
description: "Следующая процедура используется для создания производственного заказа."
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 730adcea0ac59f683ecae8cbb62025bd7db75c55
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-order"></a><span data-ttu-id="d0ffb-103">Создание производственного заказа</span><span class="sxs-lookup"><span data-stu-id="d0ffb-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0ffb-104">Следующая процедура используется для создания производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="d0ffb-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d0ffb-106">Это первая из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="d0ffb-107">Создание производственного заказа</span><span class="sxs-lookup"><span data-stu-id="d0ffb-107">Create a production order</span></span>
1. <span data-ttu-id="d0ffb-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="d0ffb-109">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-109">Click New production order.</span></span>
3. <span data-ttu-id="d0ffb-110">В поле "Код номенклатуры" введите "D0001".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="d0ffb-111">В поле "Поставка" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="d0ffb-112">Дата поставки указывает, когда должен завершиться производственный заказ для своевременной поставки.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="d0ffb-113">Эту дату можно использовать в процессе планирования.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="d0ffb-114">Например, можно запланировать заказ назад от даты поставки.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="d0ffb-115">В поле "Количество" укажите "20".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="d0ffb-116">Примечание. В поле "Код спецификации" автоматически отображается номер любой активной спецификации для текущей номенклатуры, но можно изменить спецификацию для производственного заказа, выбрав активную спецификацию из списка утвержденных версий спецификации</span><span class="sxs-lookup"><span data-stu-id="d0ffb-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="d0ffb-117">В поле "Код маршрута" автоматически отображается номер любого активного маршрута для текущей номенклатуры, но можно изменить маршрут для производственного заказа, выбрав активный маршрут из списка утвержденных версий маршрута.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="d0ffb-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="d0ffb-119">Проверка производственного заказа</span><span class="sxs-lookup"><span data-stu-id="d0ffb-119">Validate the production order</span></span>
1. <span data-ttu-id="d0ffb-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0ffb-121">Перейдите по ссылке только что созданного номера производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="d0ffb-122">Откроется страница сведений для заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="d0ffb-123">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-123">Click Edit.</span></span>
3. <span data-ttu-id="d0ffb-124">В поле "Поставка" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="d0ffb-125">Например, можно изменить дату поставки для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="d0ffb-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-126">Click Save.</span></span>
5. <span data-ttu-id="d0ffb-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="d0ffb-128">Обновление номенклатуры</span><span class="sxs-lookup"><span data-stu-id="d0ffb-128">Update the BOM</span></span>
1. <span data-ttu-id="d0ffb-129">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="d0ffb-130">Щелкните "Спецификация".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-130">Click BOM.</span></span>
    * <span data-ttu-id="d0ffb-131">Откройте страницу спецификации, чтобы проверить данные спецификации, которые были скопированы из данных по умолчанию при создании производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="d0ffb-132">В этой процедуре необходимо обновить количество для спецификации.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="d0ffb-133">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-133">Click Edit.</span></span>
4. <span data-ttu-id="d0ffb-134">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d0ffb-135">Изменение количества в строке спецификации влияет на оценку затрат потребления материалов для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="d0ffb-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-136">Click Save.</span></span>
6. <span data-ttu-id="d0ffb-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="d0ffb-138">Обновление маршрута производства</span><span class="sxs-lookup"><span data-stu-id="d0ffb-138">Update the production route</span></span>
1. <span data-ttu-id="d0ffb-139">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="d0ffb-140">Щелкните "Маршрут".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-140">Click Route.</span></span>
    * <span data-ttu-id="d0ffb-141">Откройте страницу "Маршрут", чтобы проверить данные маршрута производства, которые были скопированы из данных по умолчанию при создании заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="d0ffb-142">В этой процедуре необходимо обновить количество для одной из операции в маршруте производства.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="d0ffb-143">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d0ffb-144">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-144">Click Edit.</span></span>
5. <span data-ttu-id="d0ffb-145">В поле "К-во процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="d0ffb-146">Изменение времени процесса влияет на расчетное потребление на маршруте и затраты производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="d0ffb-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d0ffb-147">Click Save.</span></span>
7. <span data-ttu-id="d0ffb-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d0ffb-148">Close the page.</span></span>

