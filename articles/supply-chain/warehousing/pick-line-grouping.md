---
title: Группировка строк комплектации
description: В этом разделе содержится обзор группировки строк комплектации.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4436372"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="3b147-103">Группировка строк комплектации</span><span class="sxs-lookup"><span data-stu-id="3b147-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b147-104">В группировке строк комплектации несколько строк работы с одно и той же номенклатурой и местоположением могут быть объединены в единую комплектацию, которая представлена пользователю на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="3b147-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="3b147-105">Таким образом, работники склада могут получить наиболее эффективные инструкции, которые возможны, но необходимое разделение строк работы в системе также обеспечивается (например, для разных контейнеров и заказов).</span><span class="sxs-lookup"><span data-stu-id="3b147-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="3b147-106">Настройка группировки строк комплектации</span><span class="sxs-lookup"><span data-stu-id="3b147-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="3b147-107">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="3b147-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="3b147-108">Перейдите **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства** и создайте новый пункт меню, который называется **Комплектация строк группы продаж — управляется пользователем**.</span><span class="sxs-lookup"><span data-stu-id="3b147-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="3b147-109">В **Пункты меню мобильного устройства** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b147-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="3b147-110">В поле **Наименование пункта меню** введите **Комплектация продажи — строка группы**.</span><span class="sxs-lookup"><span data-stu-id="3b147-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="3b147-111">В поле **Название** введите **Комплектация продажи — строка группы**.</span><span class="sxs-lookup"><span data-stu-id="3b147-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="3b147-112">В поле **Режим** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="3b147-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="3b147-113">Укажите для **Использовать существующую работу** вариант **Да**.</span><span class="sxs-lookup"><span data-stu-id="3b147-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="3b147-114">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3b147-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="3b147-115">В поле **Кем управляется** выберите **Управляется пользователем**.</span><span class="sxs-lookup"><span data-stu-id="3b147-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="3b147-116">Установите параметр **Создать грузоместо** как **Да**.</span><span class="sxs-lookup"><span data-stu-id="3b147-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="3b147-117">Для параметра **Групповая комплектация** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3b147-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="3b147-118">На экспресс-вкладке **Классы работы** выполните следующие действия, чтобы настроить допустимые классы работы для пункта меню мобильного устройства:</span><span class="sxs-lookup"><span data-stu-id="3b147-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="3b147-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3b147-119">Select **New**.</span></span>
    2. <span data-ttu-id="3b147-120">В поле **Код класса работы** выберите **Продажи** или **Комплектация SO** в зависимости от склада, который вы будете использовать.</span><span class="sxs-lookup"><span data-stu-id="3b147-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="3b147-121">В поле **Тип заказа на работу** выберите **Заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3b147-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="3b147-122">Настройка меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="3b147-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="3b147-123">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="3b147-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="3b147-124">Добавьте только что созданный пункт меню в нужное меню.</span><span class="sxs-lookup"><span data-stu-id="3b147-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="3b147-125">Настройка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="3b147-125">Set up a work template</span></span>

1. <span data-ttu-id="3b147-126">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="3b147-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3b147-127">Найдите шаблон работы, который следует использовать с этой функцией.</span><span class="sxs-lookup"><span data-stu-id="3b147-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="3b147-128">В этом примере выберите стандартный шаблон работы Contoso **51 Pick to stage**.</span><span class="sxs-lookup"><span data-stu-id="3b147-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="3b147-129">В меню выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3b147-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="3b147-130">На вкладке **Сортировка** выберите **Добавить**, а затем установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b147-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="3b147-131">В поле **Таблица** выберите **Временные проводки работы**.</span><span class="sxs-lookup"><span data-stu-id="3b147-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="3b147-132">В поле **Производная таблица** выберите **Временные проводки работы**.</span><span class="sxs-lookup"><span data-stu-id="3b147-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="3b147-133">В поле **Поле** выберите **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="3b147-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="3b147-134">В поле **Направление поиска** выберите **Восходящее**.</span><span class="sxs-lookup"><span data-stu-id="3b147-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="3b147-135">Для работы функции группирования строк комплектации строки работы должны быть отсортированы по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b147-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="3b147-136">Если строки с одними и теми же номенклатурами не упорядочить одну за другой, они не будут сгруппированы.</span><span class="sxs-lookup"><span data-stu-id="3b147-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="3b147-137">Пример</span><span class="sxs-lookup"><span data-stu-id="3b147-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="3b147-138">Создать работы комплектации</span><span class="sxs-lookup"><span data-stu-id="3b147-138">Create picking work</span></span>

<span data-ttu-id="3b147-139">Прежде чем вы сможете настроить группировку строк комплектации, необходимо создать некоторые подходящие исходящие работы.</span><span class="sxs-lookup"><span data-stu-id="3b147-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="3b147-140">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3b147-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="3b147-141">Выберите **Создать**, чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3b147-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="3b147-142">В поле **Счет клиента** выберите любого клиента.</span><span class="sxs-lookup"><span data-stu-id="3b147-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="3b147-143">На экспресс-вкладке **Общее** в поле **Склад** выберите **51**.</span><span class="sxs-lookup"><span data-stu-id="3b147-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="3b147-144">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b147-144">Then select **OK**.</span></span>
5. <span data-ttu-id="3b147-145">В **Строки заказа на продажу** добавьте следующие шесть строк:</span><span class="sxs-lookup"><span data-stu-id="3b147-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="3b147-146">**Строка 1:** В поле **Код номенклатуры** выберите **M9200**.</span><span class="sxs-lookup"><span data-stu-id="3b147-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3b147-147">В поле **Количество** введите **3**.</span><span class="sxs-lookup"><span data-stu-id="3b147-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="3b147-148">**Строка 2:** В поле **Код номенклатуры** выберите **M9201**.</span><span class="sxs-lookup"><span data-stu-id="3b147-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="3b147-149">В поле **Количество** введите **3**.</span><span class="sxs-lookup"><span data-stu-id="3b147-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="3b147-150">**Строка 3:** В поле **Код номенклатуры** выберите **M9202**.</span><span class="sxs-lookup"><span data-stu-id="3b147-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="3b147-151">В поле **Количество** введите **2**.</span><span class="sxs-lookup"><span data-stu-id="3b147-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="3b147-152">**Строка 4:** В поле **Код номенклатуры** выберите **M9200**.</span><span class="sxs-lookup"><span data-stu-id="3b147-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3b147-153">В поле **Количество** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="3b147-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="3b147-154">**Строка 5:** В поле **Код номенклатуры** выберите **M9200**.</span><span class="sxs-lookup"><span data-stu-id="3b147-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="3b147-155">В поле **Количество** введите **3**.</span><span class="sxs-lookup"><span data-stu-id="3b147-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="3b147-156">**Строка 6:** В поле **Код номенклатуры** выберите **M9202**.</span><span class="sxs-lookup"><span data-stu-id="3b147-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="3b147-157">В поле **Количество** введите **7**.</span><span class="sxs-lookup"><span data-stu-id="3b147-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="3b147-158">Вот краткое изложение общего количества для каждого элемента:</span><span class="sxs-lookup"><span data-stu-id="3b147-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="3b147-159">**Номенклатура M9200:** 7 каждой</span><span class="sxs-lookup"><span data-stu-id="3b147-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="3b147-160">**Номенклатура M9201:** 3 каждой</span><span class="sxs-lookup"><span data-stu-id="3b147-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="3b147-161">**Номенклатура M9202:** 9 каждой</span><span class="sxs-lookup"><span data-stu-id="3b147-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="3b147-162">Перед тем, как выпустить заказы на склад, необходимо убедиться, что в местах комплектации достаточно запасов для всех номенклатур по всем заказам.</span><span class="sxs-lookup"><span data-stu-id="3b147-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="3b147-163">Просмотрите настройку **Директивы места хранения**, чтобы определить, какие ячейки комплектации используются для комплектации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="3b147-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="3b147-164">Зарезервируйте запасы и выпустите на склад.</span><span class="sxs-lookup"><span data-stu-id="3b147-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="3b147-165">Создается код работы с шестью строками.</span><span class="sxs-lookup"><span data-stu-id="3b147-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="3b147-166">Строки сортируются по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b147-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="3b147-167">Запуск потока мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="3b147-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="3b147-168">На мобильном устройстве выберите меню, включающее новый пункт меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="3b147-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="3b147-169">Выберите пункт меню **Комплектация продажи — строка группы** и инициируйте комплектацию.</span><span class="sxs-lookup"><span data-stu-id="3b147-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="3b147-170">После выбора меню и ввода идентификатора работы вы увидите шаг комплектации, в котором сгруппированы все строки выбора для номенклатуры M9200.</span><span class="sxs-lookup"><span data-stu-id="3b147-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="3b147-171">Вы получаете инструкцию по комплектации 7 номенклатур M9200.</span><span class="sxs-lookup"><span data-stu-id="3b147-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="3b147-172">Подтвердите шаг комплектации.</span><span class="sxs-lookup"><span data-stu-id="3b147-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="3b147-173">Перейдите на экран клиента выполняемой работы и обратите внимание, что все три строки комплектации для номенклатуры M9200 были закрыты одновременно.</span><span class="sxs-lookup"><span data-stu-id="3b147-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="3b147-174">Представлена строка работы 4.</span><span class="sxs-lookup"><span data-stu-id="3b147-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="3b147-175">Подтвердите шаг комплектации.</span><span class="sxs-lookup"><span data-stu-id="3b147-175">Confirm the pick step.</span></span>

    <span data-ttu-id="3b147-176">Последний шаг комплектации на мобильном устройстве агрегирует последние две строки комплектации из заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="3b147-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="3b147-177">Завершите шаг комплектации для 9 номенклатур M9202.</span><span class="sxs-lookup"><span data-stu-id="3b147-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="3b147-178">Подтвердите шаг размещения и любые дополнительные пары комплектации/размещения для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="3b147-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="3b147-179">Строки работы могут быть сгруппированы только в том случае, если они находятся в последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b147-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="3b147-180">Следующая функциональность не поддерживается:</span><span class="sxs-lookup"><span data-stu-id="3b147-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="3b147-181">Номенклатуры, учитываемые в двух единицах измерения.</span><span class="sxs-lookup"><span data-stu-id="3b147-181">Catch-weight items.</span></span> <span data-ttu-id="3b147-182">Если в работе есть какие-либо номенклатуры, учитываемые в двух единицах измерения, вы получаете сообщение об ошибке до начала комплектации.</span><span class="sxs-lookup"><span data-stu-id="3b147-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="3b147-183">Поштучная комплектация.</span><span class="sxs-lookup"><span data-stu-id="3b147-183">Piece picking.</span></span>
>    - <span data-ttu-id="3b147-184">Строки работы с незавершенной работой пополнения.</span><span class="sxs-lookup"><span data-stu-id="3b147-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="3b147-185">Комплектация с превышением.</span><span class="sxs-lookup"><span data-stu-id="3b147-185">Over-picking.</span></span>
>    - <span data-ttu-id="3b147-186">Перераспределения номенклатур для недоукомплектованности</span><span class="sxs-lookup"><span data-stu-id="3b147-186">Short picking with item reallocation</span></span>
