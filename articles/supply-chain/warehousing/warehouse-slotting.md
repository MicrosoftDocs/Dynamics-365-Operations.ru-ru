---
title: Слоттинг на складе
description: В этом разделе представлена информация о слоттинге на складе. Слоттинг на складе позволяет консолидировать спрос по номенклатуре и единицам измерения из заказов, имеющих статус "Заказанный", "Зарезервированный" или "Выпущенный". Он помогает менеджерам складов интеллектуально планировать местонахождения комплектации до того, как они выпускают заказы на склад и создают работу по комплектации.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 31b86837735ca16610a1d304eab611b12a6aceeb
ms.sourcegitcommit: be4b9d557511bbb43e71a93f2c3b23b5f1a4669d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "4627757"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="0cb3c-105">Слоттинг на складе</span><span class="sxs-lookup"><span data-stu-id="0cb3c-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cb3c-106">Несколько функций слоттинга на складе доступны, чтобы помогать менеджерам складов интеллектуально планировать местонахождения комплектации до того, как они выпускают заказы на склад и создают работу по комплектации.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="0cb3c-107">*Функция слоттинга на складе* позволяет консолидировать спрос по номенклатуре и единицам измерения из заказов, имеющих статус *Заказанный*, *Зарезервированный* или *Выпущенный*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="0cb3c-108">Созданный спрос затем может быть применен к ячейкам, которые будут использоваться для комплектации, на основе количества, единицы измерения, физических аналитик, фиксированных местоположений и т. д.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="0cb3c-109">После установки плана слоттинга можно создать работу по пополнению запасов для перемещения соответствующего объема запасов в каждое местоположение.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="0cb3c-110">Функция *Слоттинг на складе для заказов на перемещение* позволяет менеджерам склада пополнять местоположения комплектации на основе спроса из заказов на перемещение, которые еще не выпущены на склад.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="0cb3c-111">Это гарантирует, что местоположения комплектации будут включать все номенклатуры, необходимые для заказов на перемещение после их выпуска на склад.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="0cb3c-112">Для этой функции требуется также включить функцию *Функция слоттинга на складе*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="0cb3c-113">Функция *Улучшения распределения слоттинга на складе* добавляет параметр для строк шаблона, которые используются функцией *Функция слоттинга на складе*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="0cb3c-114">Параметр позволяет системе учитывать существующие запасы в наличии на целевом складе.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="0cb3c-115">Таким образом, для слоттинга может быть создано меньшее количество пополнений.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="0cb3c-116">Функция *Улучшения распределения слоттинга на складе* требует, чтобы вы также включили функцию *Функция слоттинга на складе*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="0cb3c-117">При необходимости она может использоваться совместно с функцией *Слоттинг для склада для заказов на перемещение*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="0cb3c-118">Включение функций слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0cb3c-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="0cb3c-119">Прежде чем использовать эти функции, они должны быть включены в системе.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="0cb3c-120">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса этих функций и их включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="0cb3c-121">Включите следующие функции по мере необходимости:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="0cb3c-122">Функция слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0cb3c-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="0cb3c-123">Слоттинг на складе для заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="0cb3c-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0cb3c-124">Функция *Функция слоттинга на складе* должна быть включена до этой функции.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="0cb3c-125">Усовершенствования распределения слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0cb3c-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0cb3c-126">Функция *Функция слоттинга на складе* должна быть включена до этой функции.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="0cb3c-127">Настройка слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0cb3c-127">Set up warehouse slotting</span></span>

<span data-ttu-id="0cb3c-128">Чтобы использовать слоттинг на складе, необходимо настроить следующие элементы в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="0cb3c-129">Уровни единиц измерения слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="0cb3c-130">Коды директив</span><span class="sxs-lookup"><span data-stu-id="0cb3c-130">Directive codes</span></span>
- <span data-ttu-id="0cb3c-131">Шаблоны слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-131">Slotting templates</span></span>
- <span data-ttu-id="0cb3c-132">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="0cb3c-133">Создание уровней единиц измерения для слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="0cb3c-134">Уровни единиц измерения позволяют группировать вместе несколько единиц измерения для целей слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="0cb3c-135">Например, если несколько размеров коробок все выбраны из одной области комплектации, можно создать один уровень для всех размеров.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="0cb3c-136">**Необходимо создать строку для каждой единицы измерения, которая должна быть частью уровня.**</span><span class="sxs-lookup"><span data-stu-id="0cb3c-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="0cb3c-137">Перейдите к пункту **Управление складом \> Настройка \> Пополнение \> Уровни единиц измерения слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="0cb3c-138">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-138">Select **New**.</span></span>
1. <span data-ttu-id="0cb3c-139">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-140">**Уровень единиц измерения:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="0cb3c-141">**Описание:** *Штуки коробки паллеты*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="0cb3c-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-142">Select **Save**.</span></span>
1. <span data-ttu-id="0cb3c-143">На экспресс-вкладке **Единицы измерения** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="0cb3c-144">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-145">**Единица измерения:** *Ящик*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="0cb3c-146">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0cb3c-147">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0cb3c-148">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0cb3c-149">Выберите **Создать**, чтобы добавить вторую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="0cb3c-150">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-151">**Ед. изм:** *шт.*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="0cb3c-152">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0cb3c-153">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0cb3c-154">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0cb3c-155">Выберите **Создать**, чтобы добавить третью строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="0cb3c-156">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-157">**Единица измерения:** *PL*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="0cb3c-158">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0cb3c-159">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0cb3c-160">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0cb3c-161">Выберите **Сохранить**, чтобы сохранить уровень.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="0cb3c-162">Создание кода директивы для слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-162">Create a directive code for slotting</span></span>

<span data-ttu-id="0cb3c-163">Вы должны выбрать код директивы, который должен быть связан с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="0cb3c-164">Перейдите в раздел **Управление складом \> Настройка \> Коды директив**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="0cb3c-165">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0cb3c-166">В поле **Код директивы** введите *Слоттинг*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="0cb3c-167">В поле **Описание директивы** введите *Слоттинг*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="0cb3c-168">Настройка шаблонов слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-168">Set up slotting templates</span></span>

<span data-ttu-id="0cb3c-169">Каждый шаблон слоттинга определяет способ назначения запасов местонахождениям для конкретного склада.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="0cb3c-170">Каждый шаблон должен содержать строку для каждой из спецификаций слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="0cb3c-171">Используйте процедуры данного раздела для настройки шаблонов слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="0cb3c-172">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="0cb3c-173">Выберите **Создать** для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-173">Select **New** to create a template.</span></span>

<span data-ttu-id="0cb3c-174">Затем необходимо настроить заголовок шаблона, спецификации слоттинга и директивы местоположения, как описано в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="0cb3c-175">Настройка для слоттинга для заказов на перемещение напоминает настройку для слоттинга для заказов на продажу, но в поле **Тип спроса** настраивается значение *Заказы на перемещение* вместо *Заказ на продажу*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="0cb3c-176">Настройка заголовка для шаблона слоттинга для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="0cb3c-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="0cb3c-177">В заголовке шаблона задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-178">**Шаблон слоттинга:** _61_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="0cb3c-179">**Описание:** _61_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-179">**Description:** _61_</span></span>
    - <span data-ttu-id="0cb3c-180">**Тип спроса:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="0cb3c-181">В настоящее время *Заказы на продажу* и *Заказы на перемещение* являются единственными поддерживаемыми типами спроса.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="0cb3c-182">Можно выбрать *Заказы на перемещение* только в том случае, если включена функция *Слоттинг для склада для заказов на перемещение*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="0cb3c-183">**Стратегия спроса:** _Заказано_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="0cb3c-184">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="0cb3c-185">**Заказано** — полное заказанное количество в заказе на продажу должно рассматриваться как спрос.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="0cb3c-186">**Зарезервировано** — только количества по строке заказа на продажу, которые зарезервированы (физические и заказанные), должны рассматриваться как спрос.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="0cb3c-187">**Выпущено** — выпущенное количество должно учитываться как спрос.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="0cb3c-188">**Склад:** _61_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0cb3c-189">**Разрешить волне спроса использовать незарезервированные количества:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="0cb3c-190">Можно также указать запрос для сужения области спроса, который оценивается.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="0cb3c-191">Настройка спецификаций слоттинга для каждого шаблона</span><span class="sxs-lookup"><span data-stu-id="0cb3c-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="0cb3c-192">Для каждого создаваемого шаблона заказа на продажу выполните следующие шаги, чтобы добавить строку для каждой из спецификаций слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="0cb3c-193">На экспресс-вкладке **Сведения о шаблоне слоттинга** выберите **Создать**, чтобы создать строку шаблона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="0cb3c-194">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-195">**Последовательность:** _1_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="0cb3c-196">**Описание:** _Фиксированное местоположение_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="0cb3c-197">**Минимальное количество:** _1_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="0cb3c-198">Это поле определяет минимальное количество спроса, необходимое для строки.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="0cb3c-199">**Максимальное количество:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="0cb3c-200">Это поле определяет максимальное количество спроса, допустимое для строки.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="0cb3c-201">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="0cb3c-202">Это поле определяет единицу измерения для минимального и максимального количества.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="0cb3c-203">**Уровень единиц измерения:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="0cb3c-204">Это поле определяет единицы измерения спроса, допустимые для строки.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="0cb3c-205">(Дополнительные сведения см. в разделе [Настройка уровней единиц измерения для слоттинга](#unit-tiers) ранее в этой теме.)</span><span class="sxs-lookup"><span data-stu-id="0cb3c-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="0cb3c-206">**Назначение критериев слота:** _Учитывать количество_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="0cb3c-207">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="0cb3c-208">**Считать пустым** — система должна предполагать, что все ячейки в области комплектации пусты, и не должна проверять эти ячейки на запасы.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="0cb3c-209">**Учитывать количество** — система должна проверять ячейки в области комплектации на наличие запасов, и должна пропускать все ячейки, которые не являются пустыми.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="0cb3c-210">**Учитывать запасы в наличии** — система должна проверить, содержит ли целевое местоположение нерезервированные количества для номенклатуры в строке спроса.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="0cb3c-211">Если количество является достаточным для удовлетворения по крайней мере одной единицы строки спроса, созданная запись плана слоттинга уменьшается на доступную сумму.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="0cb3c-212">Например, если спрос составляет 10 коробок, а одна коробка есть в наличии, то найденное требование составит девять коробок.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="0cb3c-213">Если спрос составляет 10 коробок, а одна штука есть в наличии, то найденное требование составит 10 коробок.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="0cb3c-214">Это значение доступно только в том случае, если включена функция *Усовершенствования распределения слоттинга на складе*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="0cb3c-215">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="0cb3c-216">Это поле определяет директиву местоположения, используемую для нахождения ячейки комплектации работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="0cb3c-217">**Местоположение переполнения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="0cb3c-218">Это поле определяет местоположение, в которое помещаются запасы, если для количества, обрабатываемого в строке, невозможно найти местоположение.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="0cb3c-219">**Разрешить освобождение:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="0cb3c-220">Если для этого параметра установлено значение *Да*, то если какой-либо спрос не может быть включен в слот, будет создана работа по перемещению, чтобы взять запасы из местоположений, где имеются запасы, но где не было использован слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="0cb3c-221">Затем шаблон запускается снова.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-221">The template is then run again.</span></span> <span data-ttu-id="0cb3c-222">На этот раз он игнорирует запасы в ячейках.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="0cb3c-223">Эта функция лучше всего работает в том случае, когда в поле **Критерии назначения слота** задано значение _Учитывать количество_.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="0cb3c-224">**Использование фиксированного местонахождения:** _Только фиксированные местонахождения для продукта_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="0cb3c-225">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="0cb3c-226">**Фиксированные и нефиксированные местонахождения** — система не должна ограничиваться использованием только фиксированных местоположений.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="0cb3c-227">**Только фиксированные местонахождения для продукта** — система должна использовать слоттинг только в местонахождениях, которые являются фиксированными местонахождениями для продукта.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="0cb3c-228">**Только фиксированные местонахождения для варианта продукта** — система должна использовать слоттинг только в местонахождениях, которые являются фиксированными местонахождениями для варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="0cb3c-229">Если шаблон слоттинга содержит по крайней мере одну строку, для которой в поле **Назначить критерий слота** задано значение *Учитывать запасы в наличии*, то допуски больше не разрешаются для любой строки шаблона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="0cb3c-230">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-230">Select **Save**.</span></span>
1. <span data-ttu-id="0cb3c-231">Выберите **Создать**, чтобы создать вторую строку шаблона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="0cb3c-232">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-233">**Последовательность:** _2_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="0cb3c-234">**Описание:** _Другое_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="0cb3c-235">**Минимальное кол-во:** _1_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="0cb3c-236">**Максимальное кол-во:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="0cb3c-237">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="0cb3c-238">**Уровень единиц измерения:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="0cb3c-239">**Назначение критериев слота:** _Учитывать количество_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="0cb3c-240">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="0cb3c-241">**Местоположение переполнения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="0cb3c-242">**Разрешить освобождение:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="0cb3c-243">**Использовать фиксированные местонахождения:** _Фиксированные и нефиксированные местонахождения_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="0cb3c-244">В запросе для второй строки будет указан критерий, который используется для определения того, в каких местоположениях может использоваться слоттинг для спроса по этой строке.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="0cb3c-245">Выберите строку, в которой в поле **Последовательность** указано значение *2*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="0cb3c-246">Выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="0cb3c-247">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0cb3c-248">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-249">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0cb3c-250">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0cb3c-251">**Поле:** *Код профиля местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="0cb3c-252">**Критерии:** *Комплектация-06* (Выберите знак двойного плюса \[**++**\] в поле, чтобы развернуть список, затем выберите *Комплектация-06* - *Сайт комплектации 6*.)</span><span class="sxs-lookup"><span data-stu-id="0cb3c-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="0cb3c-253">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="0cb3c-254">Настройка директив для места хранения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-254">Set up location directives</span></span>

<span data-ttu-id="0cb3c-255">По крайней мере одна директива местоположения должна быть настроена для поддержки комплектации со слоттингом.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="0cb3c-256">С помощью процедур данного раздела можно настроить новую *директиву местоположения пополнения* для комплектаций со слоттингом.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="0cb3c-257">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="0cb3c-258">В левой области в поле **Тип заказа на работу** выберите *Пополнение*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="0cb3c-259">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0cb3c-260">В заголовке для новой директивы местоположения в поле **Имя** введите *61 Комплектация слоттинга*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="0cb3c-261">В поле **Порядковый номер** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="0cb3c-262">Экспресс-вкладка настройки директив местоположения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="0cb3c-263">На экспресс-вкладке **Директивы местоположения** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="0cb3c-264">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0cb3c-265">**Тип работы:** _Комплектация_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="0cb3c-266">**Сайт:** _6_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-266">**Site:** _6_</span></span>
    - <span data-ttu-id="0cb3c-267">**Склад:** _61_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0cb3c-268">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="0cb3c-269">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="0cb3c-270">Экспресс-вкладка настройки строк</span><span class="sxs-lookup"><span data-stu-id="0cb3c-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="0cb3c-271">На экспресс-вкладке **Строки** выберите **Создать**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0cb3c-272">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="0cb3c-273">**Количество "От":** _0_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="0cb3c-274">**Количество "До":** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="0cb3c-275">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="0cb3c-276">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="0cb3c-277">Экспресс-вкладка настройки действий директив местоположения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="0cb3c-278">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать**, чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0cb3c-279">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-279">On the new line, set the following values.</span></span> <span data-ttu-id="0cb3c-280">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0cb3c-281">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="0cb3c-282">**Имя:** _Сборное_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="0cb3c-283">**Стратегия:** _Нет_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="0cb3c-284">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="0cb3c-285">Выберите **Сохранить**, чтобы сделать доступной кнопку **Правка запроса**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="0cb3c-286">Изменение запроса</span><span class="sxs-lookup"><span data-stu-id="0cb3c-286">Edit the query</span></span>

1. <span data-ttu-id="0cb3c-287">На экспресс-вкладке **Действия директивы местоположения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="0cb3c-288">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0cb3c-289">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-290">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0cb3c-291">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0cb3c-292">**Поле:** *Код зоны*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="0cb3c-293">**Критерии:** *Сборная* (Выберите знак двойного плюса \[**++**\] в поле, чтобы развернуть список, затем выберите *Сборная*.)</span><span class="sxs-lookup"><span data-stu-id="0cb3c-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="0cb3c-294">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="0cb3c-295">Сценарий</span><span class="sxs-lookup"><span data-stu-id="0cb3c-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="0cb3c-296">Настройка сценария</span><span class="sxs-lookup"><span data-stu-id="0cb3c-296">Set up the scenario</span></span>

<span data-ttu-id="0cb3c-297">Для этого сценария используйте встроенный пример данных и создайте записи, которые описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="0cb3c-298">Использование примера данных USMF</span><span class="sxs-lookup"><span data-stu-id="0cb3c-298">Use the USMF sample data</span></span>

<span data-ttu-id="0cb3c-299">Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3c-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0cb3c-300">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="0cb3c-301">Создание спроса</span><span class="sxs-lookup"><span data-stu-id="0cb3c-301">Create demand</span></span>

<span data-ttu-id="0cb3c-302">Выполните следующие действия, чтобы создать спрос, к которому будет применяться слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="0cb3c-303">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="0cb3c-304">Выберите **Создать**, чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="0cb3c-305">В диалоговом окне **Создать заказ на продажу** в поле **Счет клиента** выберите _US-007_.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="0cb3c-306">В поле **Склад** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0cb3c-307">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-307">Select **OK**.</span></span>
1. <span data-ttu-id="0cb3c-308">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-308">The new sales order is opened.</span></span> <span data-ttu-id="0cb3c-309">Он включает пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0cb3c-310">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-311">**Номенклатура:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="0cb3c-312">**Количество:** _20_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="0cb3c-313">Выберите **Добавить строку**, чтобы добавить новую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="0cb3c-314">**Номенклатура:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0cb3c-315">**Количество:** _8_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="0cb3c-316">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-316">Select **Save**.</span></span>
1. <span data-ttu-id="0cb3c-317">Выберите **Создать**, чтобы создать второй заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="0cb3c-318">В диалоговом окне **Создать заказ на продажу** в поле **Счет клиента** выберите _US-008_.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="0cb3c-319">В поле **Склад** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0cb3c-320">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-320">The new sales order is opened.</span></span> <span data-ttu-id="0cb3c-321">Он включает пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0cb3c-322">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="0cb3c-323">**Номенклатура:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0cb3c-324">**Количество:** _1_</span><span class="sxs-lookup"><span data-stu-id="0cb3c-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="0cb3c-325">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="0cb3c-326">Пошаговое выполнение типичного сценария слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="0cb3c-327">После того, как все необходимые элементы готовы, как описано в предыдущем разделе, можно попробовать испытать функцию, выполнив каждое из упражнений данного раздела.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="0cb3c-328">Сгенерировать спрос</span><span class="sxs-lookup"><span data-stu-id="0cb3c-328">Generate demand</span></span>

1. <span data-ttu-id="0cb3c-329">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны слоттинга** и выберите шаблон слоттинга, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="0cb3c-330">На панели операций выберите **Создать спрос**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="0cb3c-331">Эта команда оценивает весь спрос, который находится в системе, и который соответствует запросу шаблона слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="0cb3c-332">Общий спрос по всем заказам затем консолидируется в одну строку для количества/единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="0cb3c-333">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="0cb3c-334">Спрос слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-334">Slotting demand</span></span>

<span data-ttu-id="0cb3c-335">*Спрос сплоттинга* отображает результаты создания спроса на основе настройки шаблона слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="0cb3c-336">На панели операций выберите **Спрос слоттинга** для просмотра результатов из команды **Создать спрос**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="0cb3c-337">Строки в спросе слоттинга могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="0cb3c-338">Можно удалить строку, добавить новую строку или отредактировать сведения строки.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="0cb3c-339">Можно редактировать спрос вручную или импортировать его из внешней системы с помощью управления данными.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="0cb3c-340">Все, что есть в спросе слоттинга, будет использоваться на следующем шаге, независимо от того, откуда он был получен.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="0cb3c-341">Найти спрос</span><span class="sxs-lookup"><span data-stu-id="0cb3c-341">Locate demand</span></span>

<span data-ttu-id="0cb3c-342">После того как спрос был создан, следует воспользоваться командой **Найти спрос** для создания *плана слоттинга*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="0cb3c-343">На панели операций выберите **Найти спрос**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="0cb3c-344">Будет запущен процесс слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-344">The slotting process runs.</span></span> <span data-ttu-id="0cb3c-345">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="0cb3c-346">План слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-346">Slotting plan</span></span>

<span data-ttu-id="0cb3c-347">План слоттинга показывает местоположение, которому была назначена каждая номенклатура/количество, используется ли переполнение, была ли создана работа освобождения и строку шаблона, которая была использована.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="0cb3c-348">*Любой спрос, для которого невозможно использовать слоттинг, выделяется красным цветом.*</span><span class="sxs-lookup"><span data-stu-id="0cb3c-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="0cb3c-349">На панели операций выберите **План слоттинга**, чтобы просмотреть результаты.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="0cb3c-350">Процессы **Создать спрос**, **Найти спрос** и **Выполнить пополнение** теперь выполняются в "песочнице".</span><span class="sxs-lookup"><span data-stu-id="0cb3c-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="0cb3c-351">(Эти процессы доступны в области действий на странице **Шаблоны слоттинга**.)</span><span class="sxs-lookup"><span data-stu-id="0cb3c-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="0cb3c-352">Процессы **Создать спрос**, **Найти спрос** и **Выполнить пополнение** имеют блокировку, чтобы гарантировать, что они не могут быть запущены в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="0cb3c-353">В противном случае используемые данные могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="0cb3c-354">Процессы **Создание спроса** и **Найти спрос** отображают предупреждение, если в ходе выполнения не были созданы записи или если в записях отсутствуют данные.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="0cb3c-355">При выборе пункта **План слоттинга** страница не содержит кнопок **Создать**, **Изменить** или **Удалить** на панели операций, так как невозможно изменить источник данных.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="0cb3c-356">При выборе пункта **Выполнить пополнение** система проверяет выбранный шаблон слотов и процессы.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="0cb3c-357">Создание пополнения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-357">Create replenishment</span></span>

<span data-ttu-id="0cb3c-358">После создания плана слоттинга необходимо создать *работу пополнения* на основе плана.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="0cb3c-359">В области действий выберите **Выполнить пополнение**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="0cb3c-360">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="0cb3c-361">В этом сообщении указывается количество заголовков, созданных для кода сборки работы.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="0cb3c-362">Директивы местоположения, которые будут использоваться, определяются на основе кода директив, указанного в каждой строке шаблона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="0cb3c-363">Советы</span><span class="sxs-lookup"><span data-stu-id="0cb3c-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="0cb3c-364">Настройка автоматического слоттинга</span><span class="sxs-lookup"><span data-stu-id="0cb3c-364">Set up automatic slotting</span></span>

<span data-ttu-id="0cb3c-365">После того как все необходимые элементы установлены, можно настроить автоматическое выполнение слоттинга, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="0cb3c-366">Перейдите в раздел **Управление складом \> Пополнение \> Выполнение слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="0cb3c-367">Укажите шаги слоттинга для выполнения.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="0cb3c-368">Выберите один или несколько следующих шагов слоттинга:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="0cb3c-369">Сгенерировать спрос</span><span class="sxs-lookup"><span data-stu-id="0cb3c-369">Generate demand</span></span>
    - <span data-ttu-id="0cb3c-370">Найти спрос</span><span class="sxs-lookup"><span data-stu-id="0cb3c-370">Locate demand</span></span>
    - <span data-ttu-id="0cb3c-371">Создать работу пополнения</span><span class="sxs-lookup"><span data-stu-id="0cb3c-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="0cb3c-372">Шаги слоттинга прогрессивные.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-372">The slotting steps are progressive.</span></span> <span data-ttu-id="0cb3c-373">Если требуется выбрать *Поиск спроса*, необходимо сначала выбрать *Создать спрос*.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="0cb3c-374">Укажите используемый шаблон слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="0cb3c-375">При необходимости настройте повтор для автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="0cb3c-376">Для упражнений в сценарии **не** настраивайте автоматический слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
