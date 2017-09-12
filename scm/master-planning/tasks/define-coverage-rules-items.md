--- 
title: "Определение правил покрытия для номенклатур"
description: "В качестве компании с демонстрационными данными для создания этой процедуры используется USMF."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 14f56c30753da9458d66a46da8935305619fd0b8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="c8806-103">Определение правил покрытия для номенклатур</span><span class="sxs-lookup"><span data-stu-id="c8806-103">Define coverage rules for items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8806-104">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c8806-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c8806-105">В этой процедуре показано, как создать правила покрытия и переопределить параметры покрытия для определенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c8806-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="c8806-106">В ней также показано, как задать параметры запасов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8806-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="c8806-107">Создание группы покрытия</span><span class="sxs-lookup"><span data-stu-id="c8806-107">Create a coverage group</span></span>
1. <span data-ttu-id="c8806-108">Перейдите в раздел "Группы покрытия".</span><span class="sxs-lookup"><span data-stu-id="c8806-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="c8806-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c8806-109">Click New.</span></span>
3. <span data-ttu-id="c8806-110">В поле "Группа покрытия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c8806-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="c8806-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c8806-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c8806-112">В поле "Календарь" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c8806-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="c8806-113">Выберите календарь, который будет использоваться при сводном планировании для создания предложений пополнения для номенклатур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="c8806-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="c8806-114">В поле "Код покрытия" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="c8806-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="c8806-115">Для этой процедуры выберите "Потребность".</span><span class="sxs-lookup"><span data-stu-id="c8806-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="c8806-116">В поле "Временная граница покрытия (в днях)" введите значение "90".</span><span class="sxs-lookup"><span data-stu-id="c8806-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="c8806-117">Для номенклатур в этой группе при сводном планировании будут созданы предложения пополнения на 90 дней вперед.</span><span class="sxs-lookup"><span data-stu-id="c8806-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="c8806-118">В поле "Отрицательные дни" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="c8806-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="c8806-119">В поле "Положительные дни" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="c8806-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="c8806-120">Разверните или сверните раздел "Прочее".</span><span class="sxs-lookup"><span data-stu-id="c8806-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="c8806-121">В поле "Резервное время для поступления, добавленное к дате потребности" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="c8806-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="c8806-122">Например, если для поступления указано резервное время 1 день, а поступление по строке заказа на покупку запланировано на 15 мая, в сводном планировании будет указана скорректированная дата поступления 16 марта.</span><span class="sxs-lookup"><span data-stu-id="c8806-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="c8806-123">В поле "Резервное время для расхода, вычтенное из даты потребности" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="c8806-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="c8806-124">Например, если указано резервное время 1 день, а поставка по строке заказа на продажу запланирована на 15 мая, в сводном планировании будет указана скорректированная дата поставки 14 мая.</span><span class="sxs-lookup"><span data-stu-id="c8806-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="c8806-125">В поле "Резервное время для повторного заказа, добавленное ко времени упреждения для номенклатуры" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="c8806-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="c8806-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c8806-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="c8806-127">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="c8806-127">Create a new product</span></span>
1. <span data-ttu-id="c8806-128">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="c8806-128">Go to Released products.</span></span>
2. <span data-ttu-id="c8806-129">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c8806-129">Click New.</span></span>
3. <span data-ttu-id="c8806-130">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c8806-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="c8806-131">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c8806-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="c8806-132">В поле "Группа номенклатурных моделей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c8806-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c8806-133">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c8806-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c8806-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c8806-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c8806-135">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c8806-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c8806-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c8806-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c8806-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c8806-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c8806-138">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c8806-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c8806-139">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c8806-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="c8806-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c8806-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c8806-141">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c8806-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c8806-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c8806-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="c8806-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c8806-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c8806-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c8806-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="c8806-145">Настройка параметров заказов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c8806-145">Setup default order settings</span></span>
1. <span data-ttu-id="c8806-146">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="c8806-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="c8806-147">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="c8806-147">Click Default order settings.</span></span>
3. <span data-ttu-id="c8806-148">В поле "Сайт покупок" введите сайт, используемый по умолчанию при создании заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="c8806-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="c8806-149">В поле "Сайт запасов" введите сайт, где хранится номенклатура.</span><span class="sxs-lookup"><span data-stu-id="c8806-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="c8806-150">Разверните или сверните раздел "Запасы".</span><span class="sxs-lookup"><span data-stu-id="c8806-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="c8806-151">Задайте для параметра "Несколько" значение "10".</span><span class="sxs-lookup"><span data-stu-id="c8806-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="c8806-152">Задайте для параметра "Мин.</span><span class="sxs-lookup"><span data-stu-id="c8806-152">Set Min.</span></span> <span data-ttu-id="c8806-153">количество по заказу" значение "10".</span><span class="sxs-lookup"><span data-stu-id="c8806-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="c8806-154">Задайте для параметра "Макс.</span><span class="sxs-lookup"><span data-stu-id="c8806-154">Set Max.</span></span> <span data-ttu-id="c8806-155">количество по заказу" значение "100".</span><span class="sxs-lookup"><span data-stu-id="c8806-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="c8806-156">Задайте для параметра "Стандартное количество заказа" значение "10".</span><span class="sxs-lookup"><span data-stu-id="c8806-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="c8806-157">В поле "Время упреждения покупки" введите число.</span><span class="sxs-lookup"><span data-stu-id="c8806-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="c8806-158">Установите или снимите флажок "Рабочие дни".</span><span class="sxs-lookup"><span data-stu-id="c8806-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="c8806-159">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c8806-159">Click Save.</span></span>
13. <span data-ttu-id="c8806-160">В поле "Тип заказа по умолчанию" выберите "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="c8806-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="c8806-161">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c8806-161">Click Save.</span></span>
15. <span data-ttu-id="c8806-162">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c8806-162">Close the page.</span></span>
    * <span data-ttu-id="c8806-163">Закройте страницу "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="c8806-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="c8806-164">Добавление номенклатуры в группу покрытия</span><span class="sxs-lookup"><span data-stu-id="c8806-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="c8806-165">Разверните или сверните раздел "План".</span><span class="sxs-lookup"><span data-stu-id="c8806-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="c8806-166">В поле "Группа покрытия" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c8806-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c8806-167">В списке найдите созданную группу покрытия.</span><span class="sxs-lookup"><span data-stu-id="c8806-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="c8806-168">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c8806-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="c8806-169">Создание правил покрытия номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c8806-169">Create item coverage rules</span></span>
1. <span data-ttu-id="c8806-170">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="c8806-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="c8806-171">Щелкните "Покрытие номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="c8806-171">Click Item coverage.</span></span>
3. <span data-ttu-id="c8806-172">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c8806-172">Click New.</span></span>
4. <span data-ttu-id="c8806-173">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="c8806-173">Click the General tab.</span></span>
5. <span data-ttu-id="c8806-174">Установите флажок в заголовке "Переопределить параметры группы покрытия".</span><span class="sxs-lookup"><span data-stu-id="c8806-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="c8806-175">В поле "Временная граница покрытия (в днях)" введите значение "60".</span><span class="sxs-lookup"><span data-stu-id="c8806-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="c8806-176">Хотя номенклатуры в поле "Потребность" группы покрытия запланированы на 90 дней вперед, эта номенклатура будет планироваться на 60 дней вперед.</span><span class="sxs-lookup"><span data-stu-id="c8806-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="c8806-177">В поле "Отрицательные дни" введите значение "2".</span><span class="sxs-lookup"><span data-stu-id="c8806-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="c8806-178">В поле "Положительные дни" введите значение "2".</span><span class="sxs-lookup"><span data-stu-id="c8806-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="c8806-179">Перейдите на вкладку "Время упреждения".</span><span class="sxs-lookup"><span data-stu-id="c8806-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="c8806-180">Установите флажок в заголовке "Покупка".</span><span class="sxs-lookup"><span data-stu-id="c8806-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="c8806-181">В поле "Время покупки" введите значение "5".</span><span class="sxs-lookup"><span data-stu-id="c8806-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="c8806-182">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c8806-182">Click Save.</span></span>


