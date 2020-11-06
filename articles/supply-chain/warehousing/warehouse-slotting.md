---
title: Слоттинг на складе
description: В этом разделе представлена информация о слоттинге на складе. Слоттинг на складе позволяет консолидировать спрос по номенклатуре и единицам измерения из заказов, имеющих статус "Заказанный", "Зарезервированный" или "Выпущенный". Он помогает менеджерам складов интеллектуально планировать местонахождения комплектации до того, как они выпускают заказы на склад и создают работу по комплектации.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
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
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017422"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="0ca1e-105">Слоттинг на складе</span><span class="sxs-lookup"><span data-stu-id="0ca1e-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ca1e-106">Слоттинг на складе позволяет консолидировать спрос по номенклатуре и единицам измерения из заказов, имеющих статус *Заказанный* , *Зарезервированный* или *Выпущенный*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="0ca1e-107">Созданный спрос затем может быть применен к ячейкам, которые будут использоваться для комплектации, на основе количества, единицы измерения, физических аналитик, фиксированных местоположений и т. д.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="0ca1e-108">После установки плана слоттинга можно создать работу по пополнению запасов для перемещения соответствующего объема запасов в каждое местоположение.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="0ca1e-109">Эта функция помогает менеджерам складов интеллектуально планировать местонахождения комплектации до того, как они выпускают заказы на склад и создают работу по комплектации.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="0ca1e-110">Включение функции слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0ca1e-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="0ca1e-111">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0ca1e-112">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0ca1e-113">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0ca1e-114">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0ca1e-115">**Имя функции:** *Функция слоттинга на складе*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="0ca1e-116">Настройка слоттинга на складе</span><span class="sxs-lookup"><span data-stu-id="0ca1e-116">Set up warehouse slotting</span></span>

<span data-ttu-id="0ca1e-117">Чтобы использовать слоттинг на складе, необходимо настроить следующие элементы в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="0ca1e-118">Создание уровней единиц измерения для слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="0ca1e-119">Уровни единиц измерения позволяют группировать вместе несколько единиц измерения для целей слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="0ca1e-120">Например, если несколько размеров коробок все выбраны из одной области комплектации, можно создать один уровень для всех размеров.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="0ca1e-121">**Необходимо создать строку для каждой единицы измерения, которая должна быть частью уровня.**</span><span class="sxs-lookup"><span data-stu-id="0ca1e-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="0ca1e-122">Перейдите к пункту **Управление складом \> Настройка \> Пополнение \> Уровни единиц измерения слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="0ca1e-123">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-123">Select **New**.</span></span>
1. <span data-ttu-id="0ca1e-124">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-125">**Уровень единиц измерения:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="0ca1e-126">**Описание:** *Штуки коробки паллеты*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="0ca1e-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-127">Select **Save**.</span></span>
1. <span data-ttu-id="0ca1e-128">На экспресс-вкладке **Единицы измерения** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="0ca1e-129">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-130">**Единица измерения:** *Ящик*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="0ca1e-131">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0ca1e-132">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0ca1e-133">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0ca1e-134">Выберите **Создать** , чтобы добавить вторую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="0ca1e-135">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-136">**Ед. изм:** *шт.*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="0ca1e-137">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0ca1e-138">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0ca1e-139">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0ca1e-140">Выберите **Создать** , чтобы добавить третью строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="0ca1e-141">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-142">**Единица измерения:** *PL*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="0ca1e-143">**Описание:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="0ca1e-144">Оно будет заполнено автоматически при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="0ca1e-145">**Класс единиц измерения:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="0ca1e-146">Выберите **Сохранить** , чтобы сохранить уровень.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="0ca1e-147">Создание кода директивы для слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-147">Create a directive code for slotting</span></span>

<span data-ttu-id="0ca1e-148">Вы должны выбрать код директивы, который должен быть связан с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="0ca1e-149">Перейдите в раздел **Управление складом \> Настройка \> Коды директив**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="0ca1e-150">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0ca1e-151">В поле **Код директивы** введите *Слоттинг*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="0ca1e-152">В поле **Описание директивы** введите *Слоттинг*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="0ca1e-153">Настройка шаблонов слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-153">Set up slotting templates</span></span>

<span data-ttu-id="0ca1e-154">Каждый шаблон слоттинга определяет способ назначения запасов местонахождениям для конкретного склада.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="0ca1e-155">Каждый шаблон должен содержать строку для каждой из спецификаций слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="0ca1e-156">Используйте процедуры данного раздела для настройки шаблонов слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="0ca1e-157">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="0ca1e-158">Выберите **Создать** для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-158">Select **New** to create a template.</span></span>

<span data-ttu-id="0ca1e-159">Затем необходимо настроить заголовок шаблона, спецификации слоттинга и директивы местоположения, как описано в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="0ca1e-160">Настройка заголовка шаблона слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="0ca1e-161">В заголовке шаблона задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-162">**Шаблон слоттинга:** _61_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="0ca1e-163">**Описание:** _61_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-163">**Description:** _61_</span></span>
    - <span data-ttu-id="0ca1e-164">**Тип спроса:** *Заказ на продажу*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="0ca1e-165">В настоящее время *Заказ на продажу* — это единственный поддерживаемый тип спроса.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="0ca1e-166">**Стратегия спроса:** _Заказано_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="0ca1e-167">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="0ca1e-168">**Заказано** — полное заказанное количество в заказе на продажу должно рассматриваться как спрос.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="0ca1e-169">**Зарезервировано** — только количества по строке заказа на продажу, которые зарезервированы (физические и заказанные), должны рассматриваться как спрос.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="0ca1e-170">**Склад:** _61_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0ca1e-171">**Разрешить волне спроса использовать незарезервированные количества:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="0ca1e-172">Можно также указать запрос для сужения области спроса, который оценивается.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="0ca1e-173">Настройка спецификаций слоттинга для каждого шаблона</span><span class="sxs-lookup"><span data-stu-id="0ca1e-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="0ca1e-174">Для каждого создаваемого шаблона выполните следующие шаги, чтобы добавить строку для каждой из спецификаций слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="0ca1e-175">На экспресс-вкладке **Сведения о шаблоне слоттинга** выберите **Создать** , чтобы создать строку шаблона.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="0ca1e-176">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-177">**Последовательность:** _1_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="0ca1e-178">**Описание:** _Фиксированное местоположение_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="0ca1e-179">**Минимальное количество:** _1_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="0ca1e-180">Это поле определяет минимальное количество спроса, необходимое для строки.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="0ca1e-181">**Максимальное количество:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="0ca1e-182">Это поле определяет максимальное количество спроса, допустимое для строки.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="0ca1e-183">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="0ca1e-184">Это поле определяет единицу измерения для минимального и максимального количества.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="0ca1e-185">**Уровень единиц измерения:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="0ca1e-186">Это поле определяет единицы измерения спроса, допустимые для строки.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="0ca1e-187">(Дополнительные сведения см. в разделе [Настройка уровней единиц измерения для слоттинга](#unit-tiers) ранее в этой теме.)</span><span class="sxs-lookup"><span data-stu-id="0ca1e-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="0ca1e-188">**Назначение критериев слота:** _Учитывать количество_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="0ca1e-189">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="0ca1e-190">**Считать пустым** — система должна предполагать, что все ячейки в области комплектации пусты, и не должна проверять эти ячейки на запасы.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="0ca1e-191">**Учитывать количество** — система должна проверять ячейки в области комплектации на наличие запасов, и должна пропускать все ячейки, которые не являются пустыми.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="0ca1e-192">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="0ca1e-193">Это поле определяет директиву местоположения, используемую для нахождения ячейки комплектации работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="0ca1e-194">**Местоположение переполнения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="0ca1e-195">Это поле определяет местоположение, в которое помещаются запасы, если для количества, обрабатываемого в строке, невозможно найти местоположение.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="0ca1e-196">**Разрешить освобождение:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="0ca1e-197">Если для этого параметра установлено значение *Да* , то если какой-либо спрос не может быть включен в слот, будет создана работа по перемещению, чтобы взять запасы из местоположений, где имеются запасы, но где не было использован слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="0ca1e-198">Затем шаблон запускается снова.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-198">The template is then run again.</span></span> <span data-ttu-id="0ca1e-199">На этот раз он игнорирует запасы в ячейках.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="0ca1e-200">Эта функция лучше всего работает в том случае, когда в поле **Критерии назначения слота** задано значение _Учитывать количество_.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="0ca1e-201">**Использование фиксированного местонахождения:** _Только фиксированные местонахождения для продукта_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="0ca1e-202">В поле доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="0ca1e-203">**Фиксированные и нефиксированные местонахождения** — система не должна ограничиваться использованием только фиксированных местоположений.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="0ca1e-204">**Только фиксированные местонахождения для продукта** — система должна использовать слоттинг только в местонахождениях, которые являются фиксированными местонахождениями для продукта.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="0ca1e-205">**Только фиксированные местонахождения для варианта продукта** — система должна использовать слоттинг только в местонахождениях, которые являются фиксированными местонахождениями для варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="0ca1e-206">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-206">Select **Save**.</span></span>
1. <span data-ttu-id="0ca1e-207">Выберите **Создать** , чтобы создать вторую строку шаблона.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="0ca1e-208">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-209">**Последовательность:** _2_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="0ca1e-210">**Описание:** _Другое_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="0ca1e-211">**Минимальное кол-во:** _1_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="0ca1e-212">**Максимальное кол-во:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="0ca1e-213">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="0ca1e-214">**Уровень единиц измерения:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="0ca1e-215">**Назначение критериев слота:** _Учитывать количество_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="0ca1e-216">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="0ca1e-217">**Местоположение переполнения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="0ca1e-218">**Разрешить освобождение:** _Да_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="0ca1e-219">**Использовать фиксированные местонахождения:** _Фиксированные и нефиксированные местонахождения_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="0ca1e-220">В запросе для второй строки будет указан критерий, который используется для определения того, в каких местоположениях может использоваться слоттинг для спроса по этой строке.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="0ca1e-221">Выберите строку, в которой в поле **Последовательность** указано значение *2*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="0ca1e-222">Выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="0ca1e-223">На вкладке **Диапазон** выберите **Добавить** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0ca1e-224">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-225">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0ca1e-226">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0ca1e-227">**Поле:** *Код профиля местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="0ca1e-228">**Критерии:** *Комплектация-06* (Выберите знак двойного плюса \[**++**\] в поле, чтобы развернуть список, затем выберите *Комплектация-06* - *Сайт комплектации 6*.)</span><span class="sxs-lookup"><span data-stu-id="0ca1e-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="0ca1e-229">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="0ca1e-230">Настройка директив для места хранения</span><span class="sxs-lookup"><span data-stu-id="0ca1e-230">Set up location directives</span></span>

<span data-ttu-id="0ca1e-231">По крайней мере одна директива местоположения должна быть настроена для поддержки комплектации со слоттингом.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="0ca1e-232">С помощью процедур данного раздела можно настроить новую *директиву местоположения пополнения* для комплектаций со слоттингом.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="0ca1e-233">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="0ca1e-234">В левой области в поле **Тип заказа на работу** выберите *Пополнение*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="0ca1e-235">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0ca1e-236">В заголовке для новой директивы местоположения в поле **Имя** введите *61 Комплектация слоттинга*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="0ca1e-237">Экспресс-вкладка настройки директив местоположения</span><span class="sxs-lookup"><span data-stu-id="0ca1e-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="0ca1e-238">На экспресс-вкладке **Директивы местоположения** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="0ca1e-239">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0ca1e-240">**Тип работы:** _Комплектация_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="0ca1e-241">**Сайт:** _6_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-241">**Site:** _6_</span></span>
    - <span data-ttu-id="0ca1e-242">**Склад:** _61_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="0ca1e-243">**Код директивы:** _Слоттинг_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="0ca1e-244">Выберите **Сохранить** , чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="0ca1e-245">Экспресс-вкладка настройки строк</span><span class="sxs-lookup"><span data-stu-id="0ca1e-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="0ca1e-246">На экспресс-вкладке **Строки** выберите **Создать** , чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0ca1e-247">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-247">On the new line, set the following values.</span></span> <span data-ttu-id="0ca1e-248">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0ca1e-249">**Количество "От":** _0_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="0ca1e-250">**Количество "До":** _1000000_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="0ca1e-251">Выберите **Сохранить** , чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="0ca1e-252">Экспресс-вкладка настройки действий директив местоположения</span><span class="sxs-lookup"><span data-stu-id="0ca1e-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="0ca1e-253">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать** , чтобы создать строку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="0ca1e-254">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-254">On the new line, set the following values.</span></span> <span data-ttu-id="0ca1e-255">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="0ca1e-256">**Имя:** _Сборное_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="0ca1e-257">**Стратегия:** _Нет_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="0ca1e-258">Выберите **Сохранить** , чтобы сделать доступной кнопку **Правка запроса**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="0ca1e-259">Изменение запроса</span><span class="sxs-lookup"><span data-stu-id="0ca1e-259">Edit the query</span></span>

1. <span data-ttu-id="0ca1e-260">На экспресс-вкладке **Действия директивы местоположения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="0ca1e-261">На вкладке **Диапазон** выберите **Добавить** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="0ca1e-262">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-263">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="0ca1e-264">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="0ca1e-265">**Поле:** *Код зоны*</span><span class="sxs-lookup"><span data-stu-id="0ca1e-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="0ca1e-266">**Критерии:** *Сборная* (Выберите знак двойного плюса \[**++**\] в поле, чтобы развернуть список, затем выберите *Сборная*.)</span><span class="sxs-lookup"><span data-stu-id="0ca1e-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="0ca1e-267">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="0ca1e-268">Сценарий</span><span class="sxs-lookup"><span data-stu-id="0ca1e-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="0ca1e-269">Настройка сценария</span><span class="sxs-lookup"><span data-stu-id="0ca1e-269">Set up the scenario</span></span>

<span data-ttu-id="0ca1e-270">Для этого сценария используйте встроенный пример данных и создайте записи, которые описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="0ca1e-271">Использование примера данных USMF</span><span class="sxs-lookup"><span data-stu-id="0ca1e-271">Use the USMF sample data</span></span>

<span data-ttu-id="0ca1e-272">Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0ca1e-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0ca1e-273">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="0ca1e-274">Создание спроса</span><span class="sxs-lookup"><span data-stu-id="0ca1e-274">Create demand</span></span>

<span data-ttu-id="0ca1e-275">Выполните следующие действия, чтобы создать спрос, к которому будет применяться слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="0ca1e-276">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="0ca1e-277">Выберите **Создать** , чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="0ca1e-278">В диалоговом окне **Создать заказ на продажу** в поле **Счет клиента** выберите _US-007_.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="0ca1e-279">В поле **Склад** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0ca1e-280">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-280">Select **OK**.</span></span>
1. <span data-ttu-id="0ca1e-281">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-281">The new sales order is opened.</span></span> <span data-ttu-id="0ca1e-282">Он включает пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0ca1e-283">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-284">**Номенклатура:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="0ca1e-285">**Количество:** _20_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="0ca1e-286">Выберите **Добавить строку** , чтобы добавить новую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="0ca1e-287">**Номенклатура:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0ca1e-288">**Количество:** _8_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="0ca1e-289">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-289">Select **Save**.</span></span>
1. <span data-ttu-id="0ca1e-290">Выберите **Создать** , чтобы создать второй заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="0ca1e-291">В диалоговом окне **Создать заказ на продажу** в поле **Счет клиента** выберите _US-008_.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="0ca1e-292">В поле **Склад** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="0ca1e-293">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-293">The new sales order is opened.</span></span> <span data-ttu-id="0ca1e-294">Он включает пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0ca1e-295">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="0ca1e-296">**Номенклатура:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="0ca1e-297">**Количество:** _1_</span><span class="sxs-lookup"><span data-stu-id="0ca1e-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="0ca1e-298">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="0ca1e-299">Пошаговое выполнение типичного сценария слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="0ca1e-300">После того, как все необходимые элементы готовы, как описано в предыдущем разделе, можно попробовать испытать функцию, выполнив каждое из упражнений данного раздела.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="0ca1e-301">Сгенерировать спрос</span><span class="sxs-lookup"><span data-stu-id="0ca1e-301">Generate demand</span></span>

1. <span data-ttu-id="0ca1e-302">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны слоттинга** и выберите шаблон слоттинга, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="0ca1e-303">На панели операций выберите **Создать спрос**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="0ca1e-304">Эта команда оценивает весь спрос, который находится в системе, и который соответствует запросу шаблона слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="0ca1e-305">Общий спрос по всем заказам затем консолидируется в одну строку для количества/единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="0ca1e-306">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="0ca1e-307">Спрос слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-307">Slotting demand</span></span>

<span data-ttu-id="0ca1e-308">*Спрос сплоттинга* отображает результаты создания спроса на основе настройки шаблона слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="0ca1e-309">На панели операций выберите **Спрос слоттинга** для просмотра результатов из команды **Создать спрос**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="0ca1e-310">Строки в спросе слоттинга могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="0ca1e-311">Можно удалить строку, добавить новую строку или отредактировать сведения строки.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="0ca1e-312">Можно редактировать спрос вручную или импортировать его из внешней системы с помощью управления данными.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="0ca1e-313">Все, что есть в спросе слоттинга, будет использоваться на следующем шаге, независимо от того, откуда он был получен.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="0ca1e-314">Найти спрос</span><span class="sxs-lookup"><span data-stu-id="0ca1e-314">Locate demand</span></span>

<span data-ttu-id="0ca1e-315">После того как спрос был создан, следует воспользоваться командой **Найти спрос** для создания *плана слоттинга*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="0ca1e-316">На панели операций выберите **Найти спрос**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="0ca1e-317">Будет запущен процесс слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-317">The slotting process runs.</span></span> <span data-ttu-id="0ca1e-318">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="0ca1e-319">План слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-319">Slotting plan</span></span>

<span data-ttu-id="0ca1e-320">План слоттинга показывает местоположение, которому была назначена каждая номенклатура/количество, используется ли переполнение, была ли создана работа освобождения и строку шаблона, которая была использована.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="0ca1e-321">**Любой спрос, для которого невозможно использовать слоттинг, выделяется красным цветом.**</span><span class="sxs-lookup"><span data-stu-id="0ca1e-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="0ca1e-322">На панели операций выберите **План слоттинга** , чтобы просмотреть результаты.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="0ca1e-323">Создание пополнения</span><span class="sxs-lookup"><span data-stu-id="0ca1e-323">Create replenishment</span></span>

<span data-ttu-id="0ca1e-324">После создания плана слоттинга необходимо создать *работу пополнения* на основе плана.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="0ca1e-325">В области действий выберите **Выполнить пополнение**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="0ca1e-326">По завершении процесса выводится информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="0ca1e-327">В этом сообщении указывается количество заголовков, созданных для кода сборки работы.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="0ca1e-328">Директивы местоположения, которые будут использоваться, определяются на основе кода директив, указанного в каждой строке шаблона.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="0ca1e-329">Советы</span><span class="sxs-lookup"><span data-stu-id="0ca1e-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="0ca1e-330">Настройка автоматического слоттинга</span><span class="sxs-lookup"><span data-stu-id="0ca1e-330">Set up automatic slotting</span></span>

<span data-ttu-id="0ca1e-331">После того как все необходимые элементы установлены, можно настроить автоматическое выполнение слоттинга, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="0ca1e-332">Перейдите в раздел **Управление складом \> Пополнение \> Выполнение слоттинга**.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="0ca1e-333">Укажите шаги слоттинга для выполнения.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="0ca1e-334">Выберите один или несколько следующих шагов слоттинга:</span><span class="sxs-lookup"><span data-stu-id="0ca1e-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="0ca1e-335">Сгенерировать спрос</span><span class="sxs-lookup"><span data-stu-id="0ca1e-335">Generate demand</span></span>
    - <span data-ttu-id="0ca1e-336">Найти спрос</span><span class="sxs-lookup"><span data-stu-id="0ca1e-336">Locate demand</span></span>
    - <span data-ttu-id="0ca1e-337">Создать работу пополнения</span><span class="sxs-lookup"><span data-stu-id="0ca1e-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ca1e-338">Шаги слоттинга прогрессивные.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-338">The slotting steps are progressive.</span></span> <span data-ttu-id="0ca1e-339">Если требуется выбрать *Поиск спроса* , необходимо сначала выбрать *Создать спрос*.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="0ca1e-340">Укажите используемый шаблон слоттинга.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="0ca1e-341">При необходимости настройте повтор для автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="0ca1e-342">Для упражнений в сценарии **не** настраивайте автоматический слоттинг.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
