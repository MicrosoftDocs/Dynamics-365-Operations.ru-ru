---
title: Консолидация номенклатур — использование местонахождения
description: В этой теме приводятся сведения о функциональности, облегчающей менеджерам складов просмотр и фильтрацию объемного использования ячеек на складе. Менеджеры могут выбирать местоположения и создавать работу по перемещению запасов непосредственно со страницы консолидации номенклатур для консолидации номенклатур и, таким образом, лучше использовать пространство на складе.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 892190ea7bad34dfd308796b93a1828e0e8e11b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835587"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="b122f-104">Консолидация номенклатур — использование местонахождения</span><span class="sxs-lookup"><span data-stu-id="b122f-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b122f-105">В этой теме приводятся сведения о функциональности, облегчающей менеджерам складов просмотр и фильтрацию объемного использования ячеек на складе.</span><span class="sxs-lookup"><span data-stu-id="b122f-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="b122f-106">Менеджеры могут выбирать местоположения и создавать работу по перемещению запасов непосредственно со страницы **Консолидация номенклатур** для консолидации номенклатур и, таким образом, лучше использовать пространство на складе.</span><span class="sxs-lookup"><span data-stu-id="b122f-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="b122f-107">Включение функций</span><span class="sxs-lookup"><span data-stu-id="b122f-107">Turn on the features</span></span>

<span data-ttu-id="b122f-108">Прежде чем можно будет использовать функции, описанные в этой теме, их необходимо включить в системе.</span><span class="sxs-lookup"><span data-stu-id="b122f-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="b122f-109">Администраторы могут использовать рабочую область [Управление компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса этих функций и их включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="b122f-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="b122f-110">Включите обе следующих функции в том порядке, в котором они перечислены.</span><span class="sxs-lookup"><span data-stu-id="b122f-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="b122f-111">(Обе функции относятся к модулю **Управление складом**.)</span><span class="sxs-lookup"><span data-stu-id="b122f-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="b122f-112">Статус местонахождения на складе</span><span class="sxs-lookup"><span data-stu-id="b122f-112">Warehouse location status</span></span>
2. <span data-ttu-id="b122f-113">Использование местонахождения консолидации номенклатур</span><span class="sxs-lookup"><span data-stu-id="b122f-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="b122f-114">Статус местонахождения на складе</span><span class="sxs-lookup"><span data-stu-id="b122f-114">Warehouse location status</span></span>

<span data-ttu-id="b122f-115">Функция *Статус места хранения на складе* добавляет четыре новых поля на страницу **Местонахождения** для отслеживания дополнительной информации о текущем состоянии местонахождения:</span><span class="sxs-lookup"><span data-stu-id="b122f-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="b122f-116">**Код номенклатуры** — номенклатура, которая в настоящее время находится в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b122f-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="b122f-117">Если местоположение содержит несколько номенклатур, это поле будет пустым.</span><span class="sxs-lookup"><span data-stu-id="b122f-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="b122f-118">**Дата и время последнего действия** — отметка времени последней складской проводки, которая была выполнена для этого местоположения.</span><span class="sxs-lookup"><span data-stu-id="b122f-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="b122f-119">**Дата распределения по срокам** — дата, когда запасы в местонахождении поступили на склад.</span><span class="sxs-lookup"><span data-stu-id="b122f-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="b122f-120">Эта дата рассчитывается на основе даты распределения по срокам грузоместа.</span><span class="sxs-lookup"><span data-stu-id="b122f-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="b122f-121">Хотя эта дата точна для местоположений, которые отслеживаются по грузоместу, она может быть неточной для местоположений, не отслеживаемых по грузоместу.</span><span class="sxs-lookup"><span data-stu-id="b122f-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="b122f-122">**Статус местонахождения** — статус местонахождения.</span><span class="sxs-lookup"><span data-stu-id="b122f-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="b122f-123">Доступны четыре значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-123">Four values are available:</span></span>

    - <span data-ttu-id="b122f-124">**Не определено** — профиль местоположения не отслеживает статус.</span><span class="sxs-lookup"><span data-stu-id="b122f-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="b122f-125">Поэтому текущий статус неизвестен.</span><span class="sxs-lookup"><span data-stu-id="b122f-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="b122f-126">**Пусто** — в данный момент нет запасов в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="b122f-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="b122f-127">**Комплектация** — исходящие проводки для местоположения были выполнены после того как оно было пустым.</span><span class="sxs-lookup"><span data-stu-id="b122f-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="b122f-128">**Хранение** — только входящие проводки были выполнены с момента, когда оно было пустым.</span><span class="sxs-lookup"><span data-stu-id="b122f-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="b122f-129">Эти поля позволяют менеджерам склада лучше просматривать статус местоположений на складе.</span><span class="sxs-lookup"><span data-stu-id="b122f-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="b122f-130">Они также позволяют выполнять более расширенную отчетность и фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="b122f-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="b122f-131">Настройка консолидации номенклатур и использования местонахождения</span><span class="sxs-lookup"><span data-stu-id="b122f-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="b122f-132">В этом разделе описывается, как подготовить систему для использования консолидации номенклатур и использования местоположений.</span><span class="sxs-lookup"><span data-stu-id="b122f-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="b122f-133">В процедурах используются образцы значений из стандартных демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="b122f-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="b122f-134">Если планируется работа с примером сценария, представленного далее в этом разделе, выберите юридическое лицо **USMF** (которое содержит стандартные демонстрационные данные) и создайте каждую запись, описанную в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b122f-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="b122f-135">Если вы не планируете работать с примером сценария, предоставляемые здесь значения могут рассматриваться как примеры типов настройки, которую необходимо выполнить для использования этих функций.</span><span class="sxs-lookup"><span data-stu-id="b122f-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="b122f-136">Используемый продукт</span><span class="sxs-lookup"><span data-stu-id="b122f-136">Released product</span></span>

1. <span data-ttu-id="b122f-137">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="b122f-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b122f-138">В поле **Код номенклатуры** выберите *M9201* и откройте страницу сведений.</span><span class="sxs-lookup"><span data-stu-id="b122f-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="b122f-139">На панели действий на вкладке **Управление складскими запасами** в группе **Склад** выберите **Физические размеры**.</span><span class="sxs-lookup"><span data-stu-id="b122f-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="b122f-140">На странице **Физические размеры** в области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b122f-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="b122f-141">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="b122f-141">A new line is added to the grid.</span></span> <span data-ttu-id="b122f-142">Поле **Код номенклатуры** является предварительно установленным.</span><span class="sxs-lookup"><span data-stu-id="b122f-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="b122f-143">В поле **Единица измерения** выберите *шт.*</span><span class="sxs-lookup"><span data-stu-id="b122f-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="b122f-144">Оставшиеся поля в этой строке задаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="b122f-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="b122f-145">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b122f-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="b122f-146">Профиль местонахождения</span><span class="sxs-lookup"><span data-stu-id="b122f-146">Location profile</span></span>

1. <span data-ttu-id="b122f-147">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="b122f-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b122f-148">В списке профилей местоположения выберите **ЭТАЖ-05**.</span><span class="sxs-lookup"><span data-stu-id="b122f-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="b122f-149">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b122f-150">На экспресс-вкладке **Общие** убедитесь, что для обоих следующих параметров установлено значение *Да*:</span><span class="sxs-lookup"><span data-stu-id="b122f-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="b122f-151">Включить номенклатуру в месте хранения</span><span class="sxs-lookup"><span data-stu-id="b122f-151">Enable item in location</span></span>
    - <span data-ttu-id="b122f-152">Включить статус места хранения</span><span class="sxs-lookup"><span data-stu-id="b122f-152">Enable location status</span></span>

1. <span data-ttu-id="b122f-153">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b122f-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b122f-154">Если для обоих параметров **Включить номенклатуру в месте хранения** и **Включить статус места хранения** уже было задано значение *Да*, переходите дальше к инструкциям по настройке экспресс-вкладки **Аналитики** на шаге 10.</span><span class="sxs-lookup"><span data-stu-id="b122f-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="b122f-155">Если для этих параметров еще не было задано значение *Да*, необходимо выполнить проверку согласованности для модуля **Управление складом** после того, как они будут установлены вручную.</span><span class="sxs-lookup"><span data-stu-id="b122f-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="b122f-156">В этом случае перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="b122f-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="b122f-157">Чтобы выполнить проверку согласованности, перейдите к пункту **Администрирование системы \> Периодические задачи \> База данных \> Проверка целостности**.</span><span class="sxs-lookup"><span data-stu-id="b122f-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="b122f-158">В диалоговом окне **Проверка целостности** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b122f-159">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="b122f-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="b122f-160">**Режим проверки:** *Проверка*</span><span class="sxs-lookup"><span data-stu-id="b122f-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="b122f-161">**Начальная дата:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="b122f-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="b122f-162">**Проверка согласованности статуса мест хранения на складе:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="b122f-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="b122f-163">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b122f-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="b122f-164">Когда проверка целостности завершена, вы получите уведомление.</span><span class="sxs-lookup"><span data-stu-id="b122f-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="b122f-165">Откройте [центр уведомлений](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) для просмотра сообщения.</span><span class="sxs-lookup"><span data-stu-id="b122f-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="b122f-166">Выберите **Сведения о сообщении** для просмотра сведений.</span><span class="sxs-lookup"><span data-stu-id="b122f-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="b122f-167">Если в сообщении для проверки согласованности указано состояние "Найдена неверная информация о статусе места хранения для места хранения XXXX на складе XX", необходимо снова выполнить проверку согласованности.</span><span class="sxs-lookup"><span data-stu-id="b122f-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="b122f-168">На этот раз задайте в поле **Режим проверки** значение *Исправление ошибок*.</span><span class="sxs-lookup"><span data-stu-id="b122f-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="b122f-169">Просмотрите сообщения, чтобы убедиться, что не было найдено никаких ошибок.</span><span class="sxs-lookup"><span data-stu-id="b122f-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="b122f-170">Теперь необходимо завершить настройку профиля местоположения.</span><span class="sxs-lookup"><span data-stu-id="b122f-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="b122f-171">Вернитесь к пункту **Управление складом \> Настройка \> Склад \> Профили местонахождения**, выберите профиль местонахождения **ЭТАЖ-05**, затем на панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b122f-172">На экспресс-вкладке **Аналитика** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b122f-173">**Процент использования объема:** *100*</span><span class="sxs-lookup"><span data-stu-id="b122f-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="b122f-174">**Волюметрический метод, используемый для поиска местонахождения:** *Использовать объем местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b122f-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="b122f-175">**Фактическая высота места хранения:** *10*</span><span class="sxs-lookup"><span data-stu-id="b122f-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="b122f-176">**Фактическая ширина места хранения:** *10*</span><span class="sxs-lookup"><span data-stu-id="b122f-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="b122f-177">**Фактическая глубина местонахождения:** *10*</span><span class="sxs-lookup"><span data-stu-id="b122f-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="b122f-178">**Максимальный вес:** *100*</span><span class="sxs-lookup"><span data-stu-id="b122f-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="b122f-179">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b122f-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="b122f-180">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b122f-180">Mobile device menu items</span></span>

1. <span data-ttu-id="b122f-181">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b122f-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b122f-182">На панели операций выберите **Создать** для создания пункта меню для сортировки.</span><span class="sxs-lookup"><span data-stu-id="b122f-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="b122f-183">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="b122f-184">**Наименование пункта меню:** *Входящая корректировка*</span><span class="sxs-lookup"><span data-stu-id="b122f-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="b122f-185">**Заголовок:** *Входящая корректировка*</span><span class="sxs-lookup"><span data-stu-id="b122f-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="b122f-186">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="b122f-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b122f-187">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b122f-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b122f-188">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b122f-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b122f-189">**Процесс создания работы:** *Входящая корректировка*</span><span class="sxs-lookup"><span data-stu-id="b122f-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="b122f-190">**Типы корректировки запасов:** *Входящая корректировка*</span><span class="sxs-lookup"><span data-stu-id="b122f-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="b122f-191">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b122f-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="b122f-192">Меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b122f-192">Mobile device menu</span></span>

1. <span data-ttu-id="b122f-193">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b122f-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b122f-194">В списке меню выберите **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="b122f-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="b122f-195">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b122f-196">В списке **Доступные меню и пункты меню** найдите и выберите пункт меню **Входящая корректировка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="b122f-197">Выберите кнопку со стрелкой вправо, чтобы переместить пункт **Входящая корректировка** в списке **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="b122f-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="b122f-198">Таким образом, вы добавляете новый пункт меню в выбранное меню.</span><span class="sxs-lookup"><span data-stu-id="b122f-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="b122f-199">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b122f-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="b122f-200">Типы перемещения</span><span class="sxs-lookup"><span data-stu-id="b122f-200">Movement types</span></span>

1. <span data-ttu-id="b122f-201">Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Типы перемещения**.</span><span class="sxs-lookup"><span data-stu-id="b122f-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="b122f-202">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b122f-203">**Код типа перемещения:** *КОНСОЛИДИРОВАТЬ*</span><span class="sxs-lookup"><span data-stu-id="b122f-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="b122f-204">**Описание:** *Консолидация мест хранения*</span><span class="sxs-lookup"><span data-stu-id="b122f-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="b122f-205">**Код класса работы:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="b122f-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="b122f-206">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b122f-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b122f-207">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="b122f-207">Example scenario</span></span>

<span data-ttu-id="b122f-208">В следующем сценарии для выполнения *входящей корректировки* запасов в двух местах склада используется мобильное приложение управления складом.</span><span class="sxs-lookup"><span data-stu-id="b122f-208">The following scenario uses the Warehouse Management mobile app to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="b122f-209">Добавление запасов в места хранения</span><span class="sxs-lookup"><span data-stu-id="b122f-209">Add inventory to locations</span></span>

1. <span data-ttu-id="b122f-210">Выполните вход на мобильном устройстве в качестве пользователя, который настроен для склада *51*.</span><span class="sxs-lookup"><span data-stu-id="b122f-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="b122f-211">Перейти к пункту **Запасы \> Входящая корректировка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="b122f-212">Теперь будет введена первая корректировка местонахождения.</span><span class="sxs-lookup"><span data-stu-id="b122f-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="b122f-213">В задаче **Входящая корректировка** выберите местонахождение, для которого требуется выполнить корректировку запасов.</span><span class="sxs-lookup"><span data-stu-id="b122f-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="b122f-214">В поле **МЕСТОНАХОЖДЕНИЕ** выберите *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="b122f-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="b122f-215">Подтвердите местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b122f-215">Confirm the location.</span></span>
1. <span data-ttu-id="b122f-216">Создайте код грузоместа для номенклатуры, которая будет добавлен в местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b122f-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="b122f-217">В поле **Грузоместо** введите *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="b122f-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="b122f-218">Подтвердите грузоместо.</span><span class="sxs-lookup"><span data-stu-id="b122f-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="b122f-219">Введите номенклатуру, которая будет добавлена на грузоместо.</span><span class="sxs-lookup"><span data-stu-id="b122f-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="b122f-220">В поле **ITEM** введите *M9201*.</span><span class="sxs-lookup"><span data-stu-id="b122f-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="b122f-221">Подтвердите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b122f-221">Confirm the item.</span></span>
1. <span data-ttu-id="b122f-222">Введите количество номенклатуры, которое будет добавлено.</span><span class="sxs-lookup"><span data-stu-id="b122f-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="b122f-223">В поле **КОЛИЧЕСТВО** введите *10*.</span><span class="sxs-lookup"><span data-stu-id="b122f-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="b122f-224">Подтвердите количество.</span><span class="sxs-lookup"><span data-stu-id="b122f-224">Confirm the quantity.</span></span>

    <span data-ttu-id="b122f-225">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="b122f-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="b122f-226">Теперь будет введена вторая корректировка местонахождения.</span><span class="sxs-lookup"><span data-stu-id="b122f-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="b122f-227">В задаче **Входящая корректировка** выберите местонахождение, для которого требуется выполнить корректировку запасов.</span><span class="sxs-lookup"><span data-stu-id="b122f-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="b122f-228">В поле **МЕСТОНАХОЖДЕНИЕ** выберите *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="b122f-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="b122f-229">Подтвердите местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b122f-229">Confirm the location.</span></span>
1. <span data-ttu-id="b122f-230">Создайте код грузоместа для номенклатуры, которая будет добавлен в местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b122f-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="b122f-231">В поле **Грузоместо** введите *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="b122f-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="b122f-232">Подтвердите грузоместо.</span><span class="sxs-lookup"><span data-stu-id="b122f-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="b122f-233">Введите номенклатуру, которая будет добавлена на грузоместо.</span><span class="sxs-lookup"><span data-stu-id="b122f-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="b122f-234">В поле **ITEM** введите *M9201*.</span><span class="sxs-lookup"><span data-stu-id="b122f-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="b122f-235">Подтвердите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b122f-235">Confirm the item.</span></span>
1. <span data-ttu-id="b122f-236">Введите количество номенклатуры, которое будет добавлено.</span><span class="sxs-lookup"><span data-stu-id="b122f-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="b122f-237">В поле **КОЛИЧЕСТВО** введите *15*.</span><span class="sxs-lookup"><span data-stu-id="b122f-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="b122f-238">Подтвердите количество.</span><span class="sxs-lookup"><span data-stu-id="b122f-238">Confirm the quantity.</span></span>

    <span data-ttu-id="b122f-239">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="b122f-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b122f-240">Выберите кнопку меню (иногда называется "гамбургер" или "кнопка-гамбургер"), затем выберите команду **Отмена**, чтобы выйти из задачи **Входящая корректировка**.</span><span class="sxs-lookup"><span data-stu-id="b122f-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="b122f-241">Консолидация мест хранения</span><span class="sxs-lookup"><span data-stu-id="b122f-241">Consolidate locations</span></span>

1. <span data-ttu-id="b122f-242">Перейдите к пункту **Управление складом \> Периодические задачи \> Консолидация номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="b122f-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="b122f-243">В заголовке выберите склад, для которого выполняется консолидация.</span><span class="sxs-lookup"><span data-stu-id="b122f-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="b122f-244">В поле **Склад** введите *51*.</span><span class="sxs-lookup"><span data-stu-id="b122f-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="b122f-245">Запись отображается для каждой ячейки, в которой номенклатура *M9201* была скорректирована.</span><span class="sxs-lookup"><span data-stu-id="b122f-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="b122f-246">В столбце **Процент использования** указано объемное использование для каждого местонахождения.</span><span class="sxs-lookup"><span data-stu-id="b122f-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="b122f-247">Для консолидации запасов выберите все места хранения, которые необходимо консолидировать, затем в области действий выберите **Консолидировать запасы**.</span><span class="sxs-lookup"><span data-stu-id="b122f-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="b122f-248">В диалоговом окне **Консолидация запасов** укажите местонахождение и тип перемещения, которые должны использоваться для создания работы по перемещению запасов.</span><span class="sxs-lookup"><span data-stu-id="b122f-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="b122f-249">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b122f-249">Set the following values:</span></span>

    - <span data-ttu-id="b122f-250">**Местонахождение:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="b122f-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="b122f-251">**Код типа перемещения:** *КОНСОЛИДИРОВАТЬ*</span><span class="sxs-lookup"><span data-stu-id="b122f-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="b122f-252">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b122f-252">Select **OK**.</span></span>
1. <span data-ttu-id="b122f-253">Вы получаете информационное сообщение, которое показывает работу перемещения, которая была создана.</span><span class="sxs-lookup"><span data-stu-id="b122f-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="b122f-254">Запишите код работы перемещения.</span><span class="sxs-lookup"><span data-stu-id="b122f-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="b122f-255">Просмотр работы перемещения</span><span class="sxs-lookup"><span data-stu-id="b122f-255">View movement work</span></span>

1. <span data-ttu-id="b122f-256">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="b122f-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b122f-257">Просмотрите созданную работу.</span><span class="sxs-lookup"><span data-stu-id="b122f-257">View the work that was created.</span></span> <span data-ttu-id="b122f-258">Для фильтрации или поиска в сетке работ используйте код работы перемещения из консолидации запасов.</span><span class="sxs-lookup"><span data-stu-id="b122f-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="b122f-259">В этом сценарии в качестве местонахождения консолидации запасов использовалось существующее местонахождение, содержащее запасы.</span><span class="sxs-lookup"><span data-stu-id="b122f-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="b122f-260">Поэтому был создан только один код работы.</span><span class="sxs-lookup"><span data-stu-id="b122f-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="b122f-261">Система создает один код работы для каждой операции перемещения, которая должна быть завершена.</span><span class="sxs-lookup"><span data-stu-id="b122f-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="b122f-262">При указании местоположения, которое уже содержит запасы, создается только один код работы.</span><span class="sxs-lookup"><span data-stu-id="b122f-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="b122f-263">При указании нового местоположения создаются два кода работы.</span><span class="sxs-lookup"><span data-stu-id="b122f-263">If you specify a new location, two work IDs are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]