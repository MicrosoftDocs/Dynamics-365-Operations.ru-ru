---
title: Пополнение сверх объема местонахождения
description: В этом разделе приводятся сведения о функции пополнения сверх объема местонахождения. Эта функция позволяет выполнять все операции пополнения, которые необходимы для создания дня, управлять доступом к работе пополнения, чтобы гарантировать, что ячейка комплектации не будет относиться к складским запасам и не получит больше объема.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823247"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="5298a-104">Пополнение сверх объема местонахождения</span><span class="sxs-lookup"><span data-stu-id="5298a-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5298a-105">В некоторых складских запасах с ограничением объема или места должно быть отгружено большее количество номенклатуры за день, чем помещается в ячейку комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="5298a-106">Функция *Пополнение сверх объема местонахождения* позволяет выполнять все операции пополнения, которые необходимы для создания дня, управлять доступом к работе пополнения, чтобы гарантировать, что ячейка комплектации не будет относиться к складским запасам и не получит больше объема.</span><span class="sxs-lookup"><span data-stu-id="5298a-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="5298a-107">Эта функция позволяет создавать большее количество операций пополнения, чем помещается в ячейке, и блокировать работу по пополнению в случае завершения, когда местоположение заполнено.</span><span class="sxs-lookup"><span data-stu-id="5298a-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="5298a-108">Так как запасы в ячейке комплектации становятся ниже настраиваемого порогового значения, становится доступно большее количество операций пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="5298a-109">Включите функцию пополнения сверх объема местонахождения</span><span class="sxs-lookup"><span data-stu-id="5298a-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="5298a-110">Чтобы эта функция была доступна, включите следующие функции в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке):</span><span class="sxs-lookup"><span data-stu-id="5298a-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="5298a-111">Блокировка работы для всей организации</span><span class="sxs-lookup"><span data-stu-id="5298a-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="5298a-112">Пополнение сверх объема местонахождения</span><span class="sxs-lookup"><span data-stu-id="5298a-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="5298a-113">Настройка функции для примера сценария</span><span class="sxs-lookup"><span data-stu-id="5298a-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="5298a-114">В этом разделе приводятся инструкции и пример, в котором показано, как настроить эту функцию и подготовить примеры данных для сценария, приведенного ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5298a-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="5298a-115">Включение демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="5298a-115">Enable sample data</span></span>

<span data-ttu-id="5298a-116">Для работы с этими [примером сценария](#example-scenario) с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5298a-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="5298a-117">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5298a-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="5298a-118">Профиль местонахождения</span><span class="sxs-lookup"><span data-stu-id="5298a-118">Location profile</span></span>

<span data-ttu-id="5298a-119">Включите функцию пополнения сверх объема местонахождения в профиле местоположения.</span><span class="sxs-lookup"><span data-stu-id="5298a-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="5298a-120">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местоположения**.</span><span class="sxs-lookup"><span data-stu-id="5298a-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="5298a-121">В левой области выберите **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="5298a-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="5298a-122">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5298a-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5298a-123">На экспресс-вкладке **Пополнение** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5298a-124">**Превышать объем местоположения:** *Да*</span><span class="sxs-lookup"><span data-stu-id="5298a-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="5298a-125">Если включено, работе пополнения будет разрешено превышать максимальную вместимость ячейки.</span><span class="sxs-lookup"><span data-stu-id="5298a-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="5298a-126">При этом также активируется возможность включения других полей на экспресс-вкладке **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="5298a-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="5298a-127">**Тип порогового значения доступности работы:** *Количество*</span><span class="sxs-lookup"><span data-stu-id="5298a-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="5298a-128">Это поле определяет метод, который используется, чтобы определить, когда должно быть запущено большее количество работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="5298a-129">Можно выпускать по количеству или проценту:</span><span class="sxs-lookup"><span data-stu-id="5298a-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="5298a-130">*Процент* — выберите этот параметр для использования объема по проценту на основе ограничений на складе или по объему.</span><span class="sxs-lookup"><span data-stu-id="5298a-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="5298a-131">Выбор этого параметра включает поле **Процент переполнения** и отключает два поля, имеющих отношение к количеству, **Избыточное количество** и **Единица переполнения**.</span><span class="sxs-lookup"><span data-stu-id="5298a-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="5298a-132">Этот параметр можно использовать, если ячейки комплектации используют объемные показатели.</span><span class="sxs-lookup"><span data-stu-id="5298a-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="5298a-133">Если выбран этот параметр, установите в поле **Процент переполнения** значение в процентах, в течение которого будет доступно большее количество операций пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="5298a-134">*Количество* — выберите этот параметр, чтобы использовать конкретное значение количества.</span><span class="sxs-lookup"><span data-stu-id="5298a-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="5298a-135">Выбор этого параметра отключает поле **Процент переполнения** и включает два поля **Избыточное количество** и **Единица переполнения**.</span><span class="sxs-lookup"><span data-stu-id="5298a-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="5298a-136">Используйте этот параметр, если вы не используете объемные показатели для складов, для которых выполняется пополнение, или при наличии стабильных количеств, на которые требуется поместить дополнительные запасы в местоположение.</span><span class="sxs-lookup"><span data-stu-id="5298a-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="5298a-137">Если выбран этот параметр, укажите в полях **Избыточное количество** и **Единица переполнения** количество и единицу измерения, в которых будет доступно больше работы по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="5298a-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="5298a-138">**Количество переполнения:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="5298a-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="5298a-139">Это поле определяет количество, в котором переполняется местоположение.</span><span class="sxs-lookup"><span data-stu-id="5298a-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="5298a-140">Работа будет доступна, когда сумма количества в наличии в местоположении и количество работы меньше этого значения.</span><span class="sxs-lookup"><span data-stu-id="5298a-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="5298a-141">Работа пополнения, превышающая это значение, будет блокироваться, и ее нужно будет разблокировать вручную.</span><span class="sxs-lookup"><span data-stu-id="5298a-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="5298a-142">Пределы складских запасов учитываются при расчете количества работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="5298a-143">**Единица переполнения:** *PL*</span><span class="sxs-lookup"><span data-stu-id="5298a-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="5298a-144">Это поле определяет единицу измерения, связанную с количеством переполнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="5298a-145">В этом случае будет доступно большее количество операций пополнения, если ячейка имеет значение до 0,65 палеты (PL).</span><span class="sxs-lookup"><span data-stu-id="5298a-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="5298a-146">**Процент переполнения**</span><span class="sxs-lookup"><span data-stu-id="5298a-146">**Overflow percentage**</span></span>

        <span data-ttu-id="5298a-147">Это поле определяет процент, в котором переполняется местоположение.</span><span class="sxs-lookup"><span data-stu-id="5298a-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="5298a-148">Работа будет доступна, когда сумма количества в наличии в местоположении и количество работы меньше этого процента.</span><span class="sxs-lookup"><span data-stu-id="5298a-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="5298a-149">Процент количества работы пополнения, превышающий это значение, будет блокироваться, и его нужно будет разблокировать вручную.</span><span class="sxs-lookup"><span data-stu-id="5298a-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="5298a-150">Пределы складских запасов учитываются при расчете процента количества работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="5298a-151">Если лимиты хранения местонахождения не заданы, процент количества работы будет рассчитываться по объему, если в профиле местонахождения заданы ограничения по объему.</span><span class="sxs-lookup"><span data-stu-id="5298a-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5298a-152">Если используются демонстрационные данные для юридического лица **USMF** и ранее была включена функция *Позиционирование грузоместа в местонахождении*, необходимо отключить параметр **Включить позиционирование грузоместа** для профиля местоположения **BULK-06** для выполнения шагов мобильных устройств в примере сценария.</span><span class="sxs-lookup"><span data-stu-id="5298a-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="5298a-153">Код шага волны</span><span class="sxs-lookup"><span data-stu-id="5298a-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="5298a-154">Для настройки кода этапа волны, как здесь описано здесь, можно сначала использовать [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить функцию с названием *Код этапа волны для всей организации:*.</span><span class="sxs-lookup"><span data-stu-id="5298a-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="5298a-155">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Коды этапов волны**.</span><span class="sxs-lookup"><span data-stu-id="5298a-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="5298a-156">Выберите **Создать**, задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="5298a-157">**Код шага волны:** *Пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="5298a-158">**Описание этапа волны:** *Пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="5298a-159">**Тип этапа волны:** *Пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="5298a-160">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5298a-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="5298a-161">Шаблон пополнения</span><span class="sxs-lookup"><span data-stu-id="5298a-161">Replenishment template</span></span>

<span data-ttu-id="5298a-162">Шаблоны пополнения — это набор правил, определяющих когда и как пополняются местонахождения.</span><span class="sxs-lookup"><span data-stu-id="5298a-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="5298a-163">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения**.</span><span class="sxs-lookup"><span data-stu-id="5298a-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="5298a-164">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5298a-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5298a-165">В разделе **Обзор** выберите строку, в которой в поле **Шаблон пополнения** задано как значение *Пополнение для спроса*.</span><span class="sxs-lookup"><span data-stu-id="5298a-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="5298a-166">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-166">Set the following values:</span></span>

    - <span data-ttu-id="5298a-167">**Код шага волны:** *Пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="5298a-168">**Разрешить волне спроса использовать незарезервированные количества:** *Да*</span><span class="sxs-lookup"><span data-stu-id="5298a-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="5298a-169">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5298a-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="5298a-170">Шаблон волны</span><span class="sxs-lookup"><span data-stu-id="5298a-170">Wave template</span></span>

1. <span data-ttu-id="5298a-171">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="5298a-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5298a-172">В левой панели задайте в поле **Тип шаблона волн** значение *Отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="5298a-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="5298a-173">В списке выберите **61 Отгрузка**.</span><span class="sxs-lookup"><span data-stu-id="5298a-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="5298a-174">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5298a-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5298a-175">На экспресс-вкладке **Общие** установите для параметра **Автоматизировать выпуск работы пополнения** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="5298a-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="5298a-176">Установите этот параметр как *Да*, чтобы создать работу пополнения на основе запроса и автоматически запустить ее в производство.</span><span class="sxs-lookup"><span data-stu-id="5298a-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="5298a-177">Необходимо добавить метод волны пополнения в шаблон волны и создать шаблон пополнения типа **Спрос волны**.</span><span class="sxs-lookup"><span data-stu-id="5298a-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="5298a-178">Настройте шаблон пополнения на странице **Шаблоны пополнения**.</span><span class="sxs-lookup"><span data-stu-id="5298a-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="5298a-179">Для настройки шаблона пополнения необходимо добавить метод пополнения в шаблон волны.</span><span class="sxs-lookup"><span data-stu-id="5298a-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="5298a-180">На экспресс-вкладке **Методы** в столбце **Выбранные методы** найдите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="5298a-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="5298a-181">**Имя метода:** *пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="5298a-182">**Имя:** *Пополнение*</span><span class="sxs-lookup"><span data-stu-id="5298a-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="5298a-183">Задайте в поле **Код этапа волны** для этой строки значение *Пополнение*.</span><span class="sxs-lookup"><span data-stu-id="5298a-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="5298a-184">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5298a-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="5298a-185">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="5298a-185">Example scenario</span></span>

<span data-ttu-id="5298a-186">После того как вы сделали все ранее описанные образцы данных доступными и настроили их, вы можете работать с этим сценарием, чтобы попробовать функцию *Пополнение сверх объема местонахождения*.</span><span class="sxs-lookup"><span data-stu-id="5298a-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="5298a-187">Значения, показанные в этом сценарии, предполагают, что вы работаете с использованием стандартных демонстрационных данных, выбрано юридическое лицо **USMF** и подготовлены примеры записей, которые описаны ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5298a-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="5298a-188">Этот сценарий также служит в качестве примера, показывающего, как функция может использоваться в производственном параметре.</span><span class="sxs-lookup"><span data-stu-id="5298a-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="5298a-189">Создать работу пополнения</span><span class="sxs-lookup"><span data-stu-id="5298a-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="5298a-190">Создание заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="5298a-190">Create sales order 1</span></span>

1. <span data-ttu-id="5298a-191">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5298a-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5298a-192">На панели операций выберите **Создать**, чтобы открыть диалоговое окно создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="5298a-193">В диалоговом окне задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="5298a-194">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="5298a-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5298a-195">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="5298a-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5298a-196">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5298a-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="5298a-197">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-197">The new sales order is opened.</span></span> <span data-ttu-id="5298a-198">Он включает новую пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5298a-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5298a-199">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="5298a-200">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5298a-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5298a-201">**Количество:** *40*</span><span class="sxs-lookup"><span data-stu-id="5298a-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="5298a-202">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="5298a-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="5298a-203">На странице **Резервирование** выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="5298a-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="5298a-204">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5298a-204">Close the page.</span></span>
1. <span data-ttu-id="5298a-205">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="5298a-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5298a-206">Вы получаете информационные сообщения, которые показывают код волны и код отгрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="5298a-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="5298a-207">Также создается волна пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="5298a-208">Кроме того, появится предупреждающее сообщение, в котором говорится, что "Код работы XXXX не может быть разблокирован, поскольку у него есть незаконченная работу по пополнению".</span><span class="sxs-lookup"><span data-stu-id="5298a-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="5298a-209">Создание заказа на продажу 2</span><span class="sxs-lookup"><span data-stu-id="5298a-209">Create sales order 2</span></span>

1. <span data-ttu-id="5298a-210">На странице **Все заказы на продажу** на панели операций выберите **Создать**, чтобы открыть диалоговое окно создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="5298a-211">В диалоговом окне задайте следующее значение:</span><span class="sxs-lookup"><span data-stu-id="5298a-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="5298a-212">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5298a-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5298a-213">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="5298a-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5298a-214">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5298a-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="5298a-215">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-215">The new sales order is opened.</span></span> <span data-ttu-id="5298a-216">Он включает новую пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5298a-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5298a-217">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="5298a-218">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5298a-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5298a-219">**Количество:** *60*</span><span class="sxs-lookup"><span data-stu-id="5298a-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="5298a-220">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="5298a-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="5298a-221">На странице **Резервирование** выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="5298a-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="5298a-222">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5298a-222">Close the page.</span></span>
1. <span data-ttu-id="5298a-223">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="5298a-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5298a-224">Вы получаете информационные сообщения, которые показывают код волны и код отгрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="5298a-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="5298a-225">Также создается волна пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="5298a-226">Кроме того, появится предупреждающее сообщение, в котором говорится, что "Код работы XXXX не может быть разблокирован, поскольку у него есть незаконченная работу по пополнению".</span><span class="sxs-lookup"><span data-stu-id="5298a-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="5298a-227">Создание заказа на продажу 3</span><span class="sxs-lookup"><span data-stu-id="5298a-227">Create sales order 3</span></span>

1. <span data-ttu-id="5298a-228">На странице **Все заказы на продажу** на панели операций выберите **Создать**, чтобы открыть диалоговое окно создания заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="5298a-229">В диалоговом окне задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="5298a-230">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="5298a-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="5298a-231">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="5298a-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5298a-232">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5298a-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="5298a-233">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-233">The new sales order is opened.</span></span> <span data-ttu-id="5298a-234">Он включает новую пустую строку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="5298a-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5298a-235">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5298a-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="5298a-236">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5298a-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5298a-237">**Количество:** *30*</span><span class="sxs-lookup"><span data-stu-id="5298a-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="5298a-238">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="5298a-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="5298a-239">На странице **Резервирование** выберите **Зарезервировать лот**.</span><span class="sxs-lookup"><span data-stu-id="5298a-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="5298a-240">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5298a-240">Close the page.</span></span>
1. <span data-ttu-id="5298a-241">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="5298a-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="5298a-242">Вы получаете информационные сообщения, которые показывают код волны и код отгрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="5298a-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="5298a-243">Также создается волна пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="5298a-244">Кроме того, появится предупреждающее сообщение, в котором говорится, что "Код работы XXXX не может быть разблокирован, поскольку у него есть незаконченная работу по пополнению".</span><span class="sxs-lookup"><span data-stu-id="5298a-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="5298a-245">Просмотр сведений о работе</span><span class="sxs-lookup"><span data-stu-id="5298a-245">View work details</span></span>

1. <span data-ttu-id="5298a-246">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="5298a-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5298a-247">В разделе **Обзор** отфильтруйте столбец **Склад** для склада *61*.</span><span class="sxs-lookup"><span data-stu-id="5298a-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="5298a-248">Следует понять, что семь рабочих кодов были созданы для трех заказов на продажу по спросу.</span><span class="sxs-lookup"><span data-stu-id="5298a-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="5298a-249">У трех из семи кодов работы значение **Тип заказа на работу** *Пополнение*, а у четырех — значение **Тип заказа на продажу** *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="5298a-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="5298a-250">У всех трех кодов работы со значением **Тип заказа на работу** *Пополнение* одинаковые местоположения *Комплектация* и *Размещение* в разделе **Строки**:</span><span class="sxs-lookup"><span data-stu-id="5298a-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="5298a-251">**Комплектация:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="5298a-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="5298a-252">**Размещение:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="5298a-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="5298a-253">Для заказа на продажу 1 были созданы два кода работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="5298a-254">Запишите коды работы для заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="5298a-255">В зависимости от количества в наличии создаваемые количества работы могут слегка отличаться друг от друга.</span><span class="sxs-lookup"><span data-stu-id="5298a-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="5298a-256">Однако в целом, создаваемые заголовки работы должны соответствовать этому примеру сценария.</span><span class="sxs-lookup"><span data-stu-id="5298a-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="5298a-257">Код грузоместа запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="5298a-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="5298a-258">Далее в этом сценарии будет использоваться мобильное приложение управления складом (или эмулятор), где необходимо определить грузоместо для выполнения сценариев комплектации и пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-258">Later in this scenario, you will use the Warehouse Management mobile app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="5298a-259">Чтобы найти коды грузомест, которые понадобятся позднее, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5298a-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="5298a-260">Перейдите в раздел **Управление запасами \> Запросы и отчеты \> Список количества в наличии**.</span><span class="sxs-lookup"><span data-stu-id="5298a-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="5298a-261">Нажмите кнопку **Показать фильтры**, чтобы открыть панель фильтра.</span><span class="sxs-lookup"><span data-stu-id="5298a-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="5298a-262">Введите следующие критерии фильтрации, чтобы получить грузоместа для сценария.</span><span class="sxs-lookup"><span data-stu-id="5298a-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="5298a-263">Используйте фильтр *Начинается с*.</span><span class="sxs-lookup"><span data-stu-id="5298a-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="5298a-264">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="5298a-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="5298a-265">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="5298a-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="5298a-266">Выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="5298a-266">Select **Apply**.</span></span>
1. <span data-ttu-id="5298a-267">В области действий выберите **Аналитики**.</span><span class="sxs-lookup"><span data-stu-id="5298a-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="5298a-268">В диалоговом окне **Отображение аналитик** в разделе **Аналитики хранения** выберите все значения.</span><span class="sxs-lookup"><span data-stu-id="5298a-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="5298a-269">В разделе **Проводки** выберите **Код номенклатуры** и **Количество \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="5298a-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="5298a-270">После завершения нажмите кнопку **ОК**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5298a-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5298a-271">Сетка **В наличии** отображает номера грузомест для номенклатуры *T0100* в каждом местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="5298a-272">Обратите внимание на грузоместа в каждом местоположении, так как эти сведения понадобятся позже.</span><span class="sxs-lookup"><span data-stu-id="5298a-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="5298a-273">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5298a-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="5298a-274">Шаги процесса</span><span class="sxs-lookup"><span data-stu-id="5298a-274">Process steps</span></span>

<span data-ttu-id="5298a-275">Вы выполняете пополнение местоположения склада для первых двух кодов работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="5298a-276">Работа с третьим пополнением будет блокирована, пока уровень запасов в ячейке комплектации не станет ниже порогового значения.</span><span class="sxs-lookup"><span data-stu-id="5298a-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="5298a-277">Пополнение</span><span class="sxs-lookup"><span data-stu-id="5298a-277">Replenishment</span></span>

1. <span data-ttu-id="5298a-278">Выполните вход в мобильное приложение управления складом как пользователь на складе *61*.</span><span class="sxs-lookup"><span data-stu-id="5298a-278">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="5298a-279">(Введите *61* в качестве ИД пользователя и *1* в качестве пароля.)</span><span class="sxs-lookup"><span data-stu-id="5298a-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="5298a-280">Перейдите к пункту **Запасы \> Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="5298a-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="5298a-281">Вам будет предложено выполнить первую работу по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="5298a-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="5298a-282">Отображаются код номенклатуры, количество и местоположение комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="5298a-283">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="5298a-284">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="5298a-285">Система создает номер целевого грузоместа для нового грузоместа для скомплектованной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5298a-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="5298a-286">Выберите **ОК**, чтобы подтвердить значение.</span><span class="sxs-lookup"><span data-stu-id="5298a-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="5298a-287">Отображается работа размещения, как которая просит пользователя поместить целевое грузоместо в местоположение пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="5298a-288">Местоположение *Размещение* должно быть **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="5298a-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="5298a-289">Подтвердите сведения о размещении и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="5298a-290">Вы получаете сообщение "Работа завершена", и сведения о следующей задаче комплектации пополнения будут показаны: код номенклатуры, количество и местоположение, из которого будет осуществляться комплектация.</span><span class="sxs-lookup"><span data-stu-id="5298a-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="5298a-291">Ячейка комплектации будет совпадать с местоположением первого пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="5298a-292">Таким образом, у грузоместа будет один и тот же код грузоместа, который использовался для первой задачи пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="5298a-293">Повторите предыдущие шаги, чтобы завершить работу по пополнению для второй рабочей задачи.</span><span class="sxs-lookup"><span data-stu-id="5298a-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="5298a-294">Количество и целевое грузоместо должно отличаться от количества и целевого грузоместа для первой рабочей задачи.</span><span class="sxs-lookup"><span data-stu-id="5298a-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="5298a-295">После завершения работы второго пополнения будет получено сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="5298a-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5298a-296">Мобильное устройство также информирует пользователя о недоступности работы, даже если остается только одна работа по пополнению.</span><span class="sxs-lookup"><span data-stu-id="5298a-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="5298a-297">Это происходит из-за того, что работа пополнения имеет статус *На удержании* и поэтому помечается как **Заблокировано**.</span><span class="sxs-lookup"><span data-stu-id="5298a-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="5298a-298">Статус *На удержании* был присвоен, так как профиль местоположения для местоположения комплектации, которому назначена работа, имеет значение **Избыточное количество** *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="5298a-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="5298a-299">Две задачи предыдущего пополнения заполнили местоположение почти до предельного размера переполнения для номенклатуры *T0100*.</span><span class="sxs-lookup"><span data-stu-id="5298a-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="5298a-300">(Пересчет единиц измерения для номенклатуры — *1 PL = 100 шт*.) Таким образом, оставшаяся работа по пополнению приведет к превышению пределов переполнения ячейки.</span><span class="sxs-lookup"><span data-stu-id="5298a-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="5298a-301">До тех пор, пока не будет выбрано достаточное количество запасов, чтобы перевести его ниже порогового значения для работы в меню мобильного устройства, эта работа по пополнению останется заблокированной.</span><span class="sxs-lookup"><span data-stu-id="5298a-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="5298a-302">Комплектация заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="5298a-302">Sales order pick</span></span>

<span data-ttu-id="5298a-303">Прежде чем можно будет завершить остающуюся работу по пополнению, ячейка комплектации должна быть исчерпана на том уровне, на котором может быть разблокирована оставшаяся работа по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="5298a-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="5298a-304">Иными словами, сумма количества запасов в наличии в местоположении и количество пополнения не может превышать значение **Избыточное количество**.</span><span class="sxs-lookup"><span data-stu-id="5298a-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="5298a-305">Если сумма меньше, чем количество переполнения, будет разблокирована оставшаяся работа по пополнению.</span><span class="sxs-lookup"><span data-stu-id="5298a-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="5298a-306">Выполните вход в мобильное приложение управления складом как пользователь на складе *61*.</span><span class="sxs-lookup"><span data-stu-id="5298a-306">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="5298a-307">(Введите *61* в качестве ИД пользователя и *1* в качестве пароля.)</span><span class="sxs-lookup"><span data-stu-id="5298a-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="5298a-308">Выберите **Исходящие \> Комплектация продаж**.</span><span class="sxs-lookup"><span data-stu-id="5298a-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="5298a-309">Введите код первой работы для заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="5298a-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="5298a-310">См. коды работ для заказов на продажу, которые ранее были записаны на странице **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="5298a-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="5298a-311">Введенный здесь код работ создаст работу комплектации для количества 10 шт. из двух отдельных местоположений.</span><span class="sxs-lookup"><span data-stu-id="5298a-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="5298a-312">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-312">Select **OK**.</span></span>

    <span data-ttu-id="5298a-313">На странице **Заказы на продажу: размещение** отображается код номенклатуры, количество и местоположение для комплектации для первого местоположения.</span><span class="sxs-lookup"><span data-stu-id="5298a-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="5298a-314">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="5298a-315">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="5298a-316">На странице **Заказы на продажу: размещение** отображается код номенклатуры, количество и местоположение для комплектации для следующего местоположения.</span><span class="sxs-lookup"><span data-stu-id="5298a-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="5298a-317">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="5298a-318">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="5298a-319">Страница **Заказы на продажу: размещение** инструктирует о размещении завершенных работ комплектации в исходящее местоположение промежуточного хранения.</span><span class="sxs-lookup"><span data-stu-id="5298a-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="5298a-320">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-320">Select **OK**.</span></span>

    <span data-ttu-id="5298a-321">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="5298a-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="5298a-322">Введите код второй работы для заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="5298a-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="5298a-323">Для этого кода работы имеется только одна задача комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="5298a-324">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-324">Select **OK**.</span></span>

    <span data-ttu-id="5298a-325">На странице **Заказы на продажу: размещение** отображается код номенклатуры, количество и местоположение для комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="5298a-326">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="5298a-327">Указанное грузоместо будет являться одним из созданных системой грузомест из задач работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="5298a-328">Чтобы убедиться в том, что вы записали правильный код грузоместа, проверьте запасы на странице **Список количества в наличии** для номенклатуры, местоположения и количества.</span><span class="sxs-lookup"><span data-stu-id="5298a-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="5298a-329">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="5298a-330">Подтвердите инструкции для задачи размещения в исходящее местоположение промежуточного хранения.</span><span class="sxs-lookup"><span data-stu-id="5298a-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="5298a-331">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-331">Select **OK**.</span></span>

    <span data-ttu-id="5298a-332">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="5298a-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="5298a-333">Заказ на продажу 2 заблокирован для комплектации, поскольку задача пополнения, с которой он связан, не выполнена.</span><span class="sxs-lookup"><span data-stu-id="5298a-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="5298a-334">В настоящее время в ячейке комплектации по-прежнему есть 30 шт., а количество пополнения для заказа на продажу 2 — 60 шт.</span><span class="sxs-lookup"><span data-stu-id="5298a-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="5298a-335">Сумма запасов в наличии и запасов на пополнение (90 шт.) превышает избыточное количество 0,65 PL (или 65 шт.).</span><span class="sxs-lookup"><span data-stu-id="5298a-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="5298a-336">Прежде чем можно будет выполнить работу по пополнению, необходимо скомплектовать заказ на продажу 3.</span><span class="sxs-lookup"><span data-stu-id="5298a-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="5298a-337">Введите код работы для заказа на продажу 3.</span><span class="sxs-lookup"><span data-stu-id="5298a-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="5298a-338">Для этого кода работы имеется только одна задача комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="5298a-339">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-339">Select **OK**.</span></span>

    <span data-ttu-id="5298a-340">На странице **Заказы на продажу: размещение** отображается код номенклатуры, количество и местоположение для комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="5298a-341">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="5298a-342">Указанное грузоместо будет являться одним из созданных системой грузомест из задач работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="5298a-343">Чтобы убедиться в том, что вы записали правильный код грузоместа, проверьте запасы на странице **Список количества в наличии** для номенклатуры, местоположения и количества.</span><span class="sxs-lookup"><span data-stu-id="5298a-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="5298a-344">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="5298a-345">Подтвердите инструкции для задачи размещения в исходящее местоположение промежуточного хранения.</span><span class="sxs-lookup"><span data-stu-id="5298a-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="5298a-346">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-346">Select **OK**.</span></span>

    <span data-ttu-id="5298a-347">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="5298a-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="5298a-348">Как только сумма количества в наличии в местоположении комплектации и количество пополнения будет ниже порогового значения, можно будет выполнить обработку оставшейся работы по пополнению.</span><span class="sxs-lookup"><span data-stu-id="5298a-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="5298a-349">Вернитесь на страницу **Сведения о работе** и обратите внимание на то, что доступность для пополнения готовой части пополнения (для заказа на продажу 2) *Открыто*, поскольку в ячейке есть достаточно свободного места, чтобы принять пополнение.</span><span class="sxs-lookup"><span data-stu-id="5298a-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="5298a-350">Теперь можно обработать работу по пополнению, используя мобильное устройство.</span><span class="sxs-lookup"><span data-stu-id="5298a-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="5298a-351">Перейдите к пункту **Запасы \> Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="5298a-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="5298a-352">Вам будет предложено выполнить оставшуюся работу по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="5298a-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="5298a-353">Отображаются код номенклатуры, количество и местоположение комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="5298a-354">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="5298a-355">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="5298a-356">Система создает номер целевого грузоместа для нового грузоместа для скомплектованной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5298a-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="5298a-357">Выберите **ОК**, чтобы подтвердить значение.</span><span class="sxs-lookup"><span data-stu-id="5298a-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="5298a-358">Отображается работа размещения, как которая просит пользователя поместить целевое грузоместо в местоположение пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="5298a-359">Местоположение *Размещение* должно быть **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="5298a-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="5298a-360">Подтвердите сведения о размещении и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="5298a-361">Вы получаете сообщения "Работа завершена" и "Нет работы".</span><span class="sxs-lookup"><span data-stu-id="5298a-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="5298a-362">Теперь можно скомплектовать заказ на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="5298a-362">You can now pick sales order 2.</span></span> <span data-ttu-id="5298a-363">Он был разблокирован после выполнения работы по пополнению, связанной с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="5298a-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="5298a-364">Введите код работы для заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="5298a-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="5298a-365">Для этого кода работы имеется только одна задача комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="5298a-366">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-366">Select **OK**.</span></span>

    <span data-ttu-id="5298a-367">На странице **Заказы на продажу: размещение** отображается код номенклатуры, количество и местоположение для комплектации.</span><span class="sxs-lookup"><span data-stu-id="5298a-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="5298a-368">В поле **LP** введите номер грузоместа для номенклатуры в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="5298a-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="5298a-369">Указанное грузоместо будет являться созданным системой грузоместом из задачи работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="5298a-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="5298a-370">Чтобы убедиться в том, что вы записали правильный код грузоместа, проверьте запасы на странице **Список количества в наличии** для номенклатуры, местоположения и количества.</span><span class="sxs-lookup"><span data-stu-id="5298a-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="5298a-371">Нажмите кнопку **ОК** (символ галочки).</span><span class="sxs-lookup"><span data-stu-id="5298a-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="5298a-372">Подтвердите инструкции для задачи размещения в исходящее местоположение промежуточного хранения.</span><span class="sxs-lookup"><span data-stu-id="5298a-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="5298a-373">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5298a-373">Select **OK**.</span></span>

    <span data-ttu-id="5298a-374">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="5298a-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="5298a-375">Примечания и советы</span><span class="sxs-lookup"><span data-stu-id="5298a-375">Notes and tips</span></span>

- <span data-ttu-id="5298a-376">Эта функция применима для всех типов пополнения: спрос волны, мин/макс, спрос загрузки и слоттинг.</span><span class="sxs-lookup"><span data-stu-id="5298a-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="5298a-377">При необходимости можно вручную переопределить доступность для пополнения для каждого заголовка работ на странице **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="5298a-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="5298a-378">Когда система устанавливает доступность по пополнению запасов, она учитывает все складские запасы, которые уже находятся в местоположении до завершения любой работы.</span><span class="sxs-lookup"><span data-stu-id="5298a-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="5298a-379">Каждая часть работы с заказами на продажу связана с определенной работой по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="5298a-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="5298a-380">Нет соответствующих функций для работы с продажами.</span><span class="sxs-lookup"><span data-stu-id="5298a-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]