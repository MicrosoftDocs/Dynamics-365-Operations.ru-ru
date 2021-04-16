---
title: Группировка строк комплектации
description: В этом разделе содержится обзор группировки строк комплектации.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828282"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="f34eb-103">Группировка строк комплектации</span><span class="sxs-lookup"><span data-stu-id="f34eb-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f34eb-104">Группировка строк комплектации позволяет несколько строк работы с одной и той же номенклатурой и местоположением объединить в единую комплектацию, которая представлена пользователю на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f34eb-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="f34eb-105">Таким образом, работники склада могут получить наиболее эффективные инструкции, но необходимое разделение строк работы (для разных контейнеров, заказов и т. д.) все равно может поддерживаться в системе.</span><span class="sxs-lookup"><span data-stu-id="f34eb-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="f34eb-106">Включение функции группирования строк комплектации</span><span class="sxs-lookup"><span data-stu-id="f34eb-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="f34eb-107">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="f34eb-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f34eb-108">Администраторы могут использовать рабочую область [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса этой функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="f34eb-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f34eb-109">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f34eb-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f34eb-110">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="f34eb-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f34eb-111">**Название компонента:** *Группировка строк комплектации*</span><span class="sxs-lookup"><span data-stu-id="f34eb-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="f34eb-112">Настройка группировки строк комплектации</span><span class="sxs-lookup"><span data-stu-id="f34eb-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="f34eb-113">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="f34eb-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="f34eb-114">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f34eb-115">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f34eb-116">В поле **Наименование пункта меню** введите *Комплектация строк группы продаж*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="f34eb-117">В поле **Название** введите *Комплектация строк группы продаж*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="f34eb-118">Этот заголовок будет отображаться в меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="f34eb-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="f34eb-119">В поле **Режим** выберите *Работа*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="f34eb-120">Укажите для **Использовать существующую работу** вариант *Да*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="f34eb-121">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f34eb-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f34eb-122">В поле **Кем управляется** выберите *Управляется пользователем*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="f34eb-123">Установите параметр **Создать грузоместо** как *Да*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="f34eb-124">Для параметра **Групповая комплектация** выберите значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="f34eb-125">Примите значения по умолчанию для остальных параметров.</span><span class="sxs-lookup"><span data-stu-id="f34eb-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="f34eb-126">Выполните следующие действия, чтобы настроить допустимые классы работы для пункта меню мобильного устройства:</span><span class="sxs-lookup"><span data-stu-id="f34eb-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="f34eb-127">На экспресс-вкладке **Классы работы** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="f34eb-128">В поле **Код класса работы** можно выбрать *Продажи* или *Комплектация SO* в зависимости от склада, который вы будете использовать.</span><span class="sxs-lookup"><span data-stu-id="f34eb-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="f34eb-129">Для этого сценария выберите *Комплектация SO*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="f34eb-130">В поле **Тип заказа на работу** автоматически задается значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="f34eb-131">Настройка меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="f34eb-131">Set up a mobile device menu</span></span>

<span data-ttu-id="f34eb-132">Выполните следующие действия, чтобы добавить только что созданный пункт меню в меню **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="f34eb-133">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="f34eb-134">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f34eb-135">В области списка отображаются все существующие меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="f34eb-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="f34eb-136">Выберите *Исходящие* в списке.</span><span class="sxs-lookup"><span data-stu-id="f34eb-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="f34eb-137">В списке **Доступные меню и пункты меню** найдите и выберите только что созданный пункт меню *Комплектация строк группы продаж*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="f34eb-138">Нажмите кнопку со стрелкой вправо, чтобы переместить пункт меню *Комплектация строк группы продаж* в список **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="f34eb-139">Используйте кнопки со стрелкой вверх и вниз для перемещения пункта меню в нужную позицию в структуре меню.</span><span class="sxs-lookup"><span data-stu-id="f34eb-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="f34eb-140">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="f34eb-141">Настройка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="f34eb-141">Set up a work template</span></span>

1. <span data-ttu-id="f34eb-142">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f34eb-143">В поле **Тип заказа на работу** выберите *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="f34eb-144">В сетке **Обзора** найдите и выберите рабочий шаблон, который должен использоваться с этой функцией.</span><span class="sxs-lookup"><span data-stu-id="f34eb-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="f34eb-145">Для этого сценария выберите шаблон *51 Скомплектовать для стадии*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="f34eb-146">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f34eb-147">В диалоговом окне редактора запросов на вкладке **Сортировка** выберите **Добавить**,, затем установите следующие значения для новой строки:</span><span class="sxs-lookup"><span data-stu-id="f34eb-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="f34eb-148">В столбце **Таблица** выберите *Временные проводки работы*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="f34eb-149">В столбце **Производная таблица** выберите *Временные проводки работы*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="f34eb-150">В столбце **Поле** выберите *Код номенклатуры*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="f34eb-151">В столбце **Направление поиска** выберите *Восходящее*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="f34eb-152">Выберите **ОК**, чтобы закрыть диалоговое окно и сохранить ваш выбор.</span><span class="sxs-lookup"><span data-stu-id="f34eb-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="f34eb-153">Появится следующее сообщение: "Группирование будет сброшено, продолжить?"</span><span class="sxs-lookup"><span data-stu-id="f34eb-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="f34eb-154">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="f34eb-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f34eb-155">Для работы функции группирования строк комплектации строки работы должны быть отсортированы по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f34eb-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="f34eb-156">Если строки с одними и теми же номенклатурами не упорядочить одну за другой, они не будут сгруппированы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="f34eb-157">Пример</span><span class="sxs-lookup"><span data-stu-id="f34eb-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="f34eb-158">Создать работы комплектации</span><span class="sxs-lookup"><span data-stu-id="f34eb-158">Create picking work</span></span>

<span data-ttu-id="f34eb-159">Прежде чем вы сможете настроить группировку строк комплектации, необходимо создать некоторые подходящие исходящие работы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="f34eb-160">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f34eb-161">Выберите **Создать**, чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="f34eb-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f34eb-162">В поле **Счет клиента** выберите *US-004*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="f34eb-163">На экспресс-вкладке **Общее** в поле **Склад** выберите *51*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="f34eb-164">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-164">Select **OK**.</span></span>
1. <span data-ttu-id="f34eb-165">На экспресс-вкладке **Строки заказа на продажу** добавьте следующие шесть строк:</span><span class="sxs-lookup"><span data-stu-id="f34eb-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="f34eb-166">**Строка 1:** В поле **Код номенклатуры** выберите *M9200*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="f34eb-167">В поле **Количество** введите *3*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="f34eb-168">**Строка 2:** В поле **Код номенклатуры** выберите *M9201*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="f34eb-169">В поле **Количество** введите *3*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="f34eb-170">**Строка 3:** В поле **Код номенклатуры** выберите *M9202*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="f34eb-171">В поле **Количество** введите *2*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="f34eb-172">**Строка 4:** В поле **Код номенклатуры** выберите *M9200*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="f34eb-173">В поле **Количество** введите *1*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="f34eb-174">**Строка 5:** В поле **Код номенклатуры** выберите *M9200*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="f34eb-175">В поле **Количество** введите *3*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="f34eb-176">**Строка 6:** В поле **Код номенклатуры** выберите *M9202*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="f34eb-177">В поле **Количество** введите *7*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="f34eb-178">Вот краткое изложение общего количества для каждого элемента:</span><span class="sxs-lookup"><span data-stu-id="f34eb-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="f34eb-179">**Номенклатура M9200:** *7* каждой</span><span class="sxs-lookup"><span data-stu-id="f34eb-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="f34eb-180">**Номенклатура M9201:** *3* каждой</span><span class="sxs-lookup"><span data-stu-id="f34eb-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="f34eb-181">**Номенклатура M9202:** *9* каждой</span><span class="sxs-lookup"><span data-stu-id="f34eb-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="f34eb-182">Перед тем, как выпустить заказы на склад, необходимо убедиться, что в местах комплектации достаточно запасов для всех номенклатур по всем заказам.</span><span class="sxs-lookup"><span data-stu-id="f34eb-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="f34eb-183">Просмотрите настройку **Директивы места хранения**, чтобы определить, какие ячейки комплектации используются для комплектации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="f34eb-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="f34eb-184">Если вы используете среду демонстрационных данных Contoso для склада *51*, убедитесь в наличии доступных запасов.</span><span class="sxs-lookup"><span data-stu-id="f34eb-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="f34eb-185">Теперь необходимо резервировать запасы для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="f34eb-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="f34eb-186">На экспресс-вкладке **Строки заказа на продажу** выберите одну из строк, которые необходимо зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="f34eb-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="f34eb-187">В меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f34eb-188">На странице **Резервирование** на панели операций выберите **Резервирование лота** для применения резервирования.</span><span class="sxs-lookup"><span data-stu-id="f34eb-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="f34eb-189">Затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f34eb-189">Then close the page.</span></span>
1. <span data-ttu-id="f34eb-190">Повторите шаги с 8 по 10 для остальных строк, которые должны быть зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="f34eb-191">Теперь необходимо выпустить заказ на продажу на склад.</span><span class="sxs-lookup"><span data-stu-id="f34eb-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="f34eb-192">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f34eb-193">Появится сообщение о том, что была создана отгрузка и волна, и что запись волны была отправлена для выполнения в пакете.</span><span class="sxs-lookup"><span data-stu-id="f34eb-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="f34eb-194">Когда волна и все нижестоящие задания заполнены, для работы, которая имеет шесть строк, создается код работы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="f34eb-195">Строки сортируются по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f34eb-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="f34eb-196">Перейдите в раздел **Управление складом \> Работа \> Вся работа** для просмотра созданной работы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="f34eb-197">Запишите значение **Код работы**, поскольку он потребуется в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="f34eb-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="f34eb-198">Инициация комплектации с мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="f34eb-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="f34eb-199">Выполните вход на мобильном устройстве в качестве пользователя, который настроен для склада *51*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="f34eb-200">На мобильном устройстве выберите меню, включающее новый пункт меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="f34eb-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="f34eb-201">Для этого сценария выберите **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="f34eb-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="f34eb-202">Выберите пункт меню **Комплектация строки группы продаж**, чтобы инициировать комплектацию.</span><span class="sxs-lookup"><span data-stu-id="f34eb-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="f34eb-203">Введите значения **Код работы**, которое вы записали в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="f34eb-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="f34eb-204">Должен отобразиться шаг комплектации, где группируются все строки комплектации для номенклатуры *M9200*, и должна получить инструкцию для комплектации *7* штук номенклатуры *M9200*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f34eb-205">На мобильном устройстве работа по комплектации для трех строк работы комплектации была агрегирована в один шаг комплектации для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f34eb-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="f34eb-206">Подтвердите шаг комплектации.</span><span class="sxs-lookup"><span data-stu-id="f34eb-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="f34eb-207">Перейдите на страницу работы для кода работы и обратите внимание, что все три строки комплектации для номенклатуры *M9200* были закрыты одновременно.</span><span class="sxs-lookup"><span data-stu-id="f34eb-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="f34eb-208">Вернитесь на мобильное устройство и продолжите комплектацию.</span><span class="sxs-lookup"><span data-stu-id="f34eb-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="f34eb-209">Должна быть представлена строка работы 4 штук номенклатуры *M9201*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="f34eb-210">Так как в заказе была только одна строка, агрегировать ничего.</span><span class="sxs-lookup"><span data-stu-id="f34eb-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="f34eb-211">Подтвердите шаг комплектации.</span><span class="sxs-lookup"><span data-stu-id="f34eb-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="f34eb-212">Последний шаг комплектации на мобильном устройстве агрегирует последние две строки комплектации из заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="f34eb-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="f34eb-213">Завершите шаг комплектации для *9* штук номенклатуры *M9202*.</span><span class="sxs-lookup"><span data-stu-id="f34eb-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="f34eb-214">Подтвердите шаг размещения и любые дополнительные пары комплектации/размещения для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="f34eb-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="f34eb-215">Строки работы могут быть сгруппированы только в том случае, если они находятся в последовательности.</span><span class="sxs-lookup"><span data-stu-id="f34eb-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="f34eb-216">Следующая функциональность не поддерживается:</span><span class="sxs-lookup"><span data-stu-id="f34eb-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="f34eb-217">Номенклатуры, учитываемые в двух единицах измерения</span><span class="sxs-lookup"><span data-stu-id="f34eb-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="f34eb-218">Если в работе есть какие-либо номенклатуры, учитываемые в двух единицах измерения, вы получаете сообщение об ошибке до начала комплектации.</span><span class="sxs-lookup"><span data-stu-id="f34eb-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="f34eb-219">Поштучная комплектация</span><span class="sxs-lookup"><span data-stu-id="f34eb-219">Piece picking</span></span>
>   - <span data-ttu-id="f34eb-220">Строки работы с незавершенной работой пополнения</span><span class="sxs-lookup"><span data-stu-id="f34eb-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="f34eb-221">Комплектация с превышением</span><span class="sxs-lookup"><span data-stu-id="f34eb-221">Over-picking</span></span>
>   - <span data-ttu-id="f34eb-222">Перераспределения номенклатур для недоукомплектованности</span><span class="sxs-lookup"><span data-stu-id="f34eb-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]