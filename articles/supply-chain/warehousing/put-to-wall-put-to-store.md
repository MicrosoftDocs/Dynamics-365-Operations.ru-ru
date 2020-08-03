---
title: Поместить на стену — поместить в магазин
description: В этой теме приводятся сведения о функциональности "Поместить на стену — поместить в магазин". Эта функция позволяет обрабатывать сценарии, в которых необходимо консолидировать продукт в промежуточной области предварительной упаковки, используя настраиваемые критерии. Оно помогает уменьшить время комплектации, поскольку допускает комплектацию на одном целевом грузоместе и может использовать больше позиций размещения, чем кластерная комплектация.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 10eb32f75ccfe1521af9ebfe1e73ef08ea4238f7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597559"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="1adb7-105">Поместить на стену — поместить в магазин</span><span class="sxs-lookup"><span data-stu-id="1adb7-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1adb7-106">Функция *Поместить на стену — поместить в магазин* позволяет обрабатывать сценарии, в которых необходимо консолидировать продукт в промежуточной области предварительной упаковки, используя настраиваемые критерии.</span><span class="sxs-lookup"><span data-stu-id="1adb7-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="1adb7-107">Так как эта функция позволяет комплектацию на одном целевом грузоместе и может использовать больше позиций размещения, чем комплектация кластера, компании, которые отгружают в магазины или обрабатывают небольшие номенклатуры, смогут получить преимущества от уменьшения времени комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="1adb7-108">Рабочий процесс для этой функциональности направляет отобранный продукт на место сортировки для распределения по различным типам контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1adb7-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="1adb7-109">Обычно каждое местоположение сортировки содержит несколько позиций сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="1adb7-110">Каждая позиция сортировки назначается в соответствии с критерием, заданным бизнес-процессом.</span><span class="sxs-lookup"><span data-stu-id="1adb7-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="1adb7-111">Обычно в качестве критерия используется конечная точка, отгрузка или загрузка.</span><span class="sxs-lookup"><span data-stu-id="1adb7-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="1adb7-112">После прибытия продукта он распределяется по каждой позиции сортировки на основе количества, связанного с заказом, пунктом назначения, отгрузкой или загрузкой.</span><span class="sxs-lookup"><span data-stu-id="1adb7-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="1adb7-113">Когда контейнер заполнен или завершен, он перемещается в промежуточное местоположение или место отгрузки для дальнейшей обработки, в зависимости от бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="1adb7-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="1adb7-114">Эти функции склада также называются другими названиями, такими как световые подсказки и перерыв.</span><span class="sxs-lookup"><span data-stu-id="1adb7-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="1adb7-115">Включение функции исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="1adb7-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="1adb7-116">Прежде чем можно будет использовать функцию *Поместить на стену — поместить в магазин*, в системе должна быть включена функция *исходящей сортировки*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="1adb7-117">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="1adb7-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1adb7-118">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1adb7-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1adb7-119">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="1adb7-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1adb7-120">**Название компонента:** *Исходящая сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="1adb7-121">Функция *исходящей сортировки* может использоваться в сочетании с функцией *кода этапа волны для всей организации*, если она включена.</span><span class="sxs-lookup"><span data-stu-id="1adb7-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="1adb7-122">Кроме того, необходимо включить эту функцию, если будут использоваться заранее определенные коды, настроенные в кодах этапов волн.</span><span class="sxs-lookup"><span data-stu-id="1adb7-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="1adb7-123">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="1adb7-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="1adb7-124">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="1adb7-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1adb7-125">**Имя функции:** *Код этапа волны для всей организации*</span><span class="sxs-lookup"><span data-stu-id="1adb7-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="1adb7-126">Настройка</span><span class="sxs-lookup"><span data-stu-id="1adb7-126">Setup</span></span>

<span data-ttu-id="1adb7-127">Для этой демонстрации используются стандартные данные Contoso и склад *62*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="1adb7-128">Кроме того, будут использованы некоторые добавления, отмеченные позже.</span><span class="sxs-lookup"><span data-stu-id="1adb7-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="1adb7-129">Тип местоположения</span><span class="sxs-lookup"><span data-stu-id="1adb7-129">Location type</span></span>

1. <span data-ttu-id="1adb7-130">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Типы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="1adb7-131">На панели операций выберите **Создать** для создания типа местонахождения для сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="1adb7-132">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-132">Set the following values:</span></span>

    - <span data-ttu-id="1adb7-133">**Тип местоположения:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="1adb7-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="1adb7-134">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="1adb7-135">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="1adb7-136">Параметры управления складом</span><span class="sxs-lookup"><span data-stu-id="1adb7-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="1adb7-137">Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="1adb7-138">На вкладке **Общие** на экспресс-вкладке **Типы местонахождения** введите в поле **Тип местонахождения сортировки** значение *СОРТИРОВКА*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="1adb7-139">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="1adb7-140">Профиль местонахождения</span><span class="sxs-lookup"><span data-stu-id="1adb7-140">Location profile</span></span>

1. <span data-ttu-id="1adb7-141">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="1adb7-142">На панели операций выберите **Создать** для создания профиля местонахождения для местонахождения сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="1adb7-143">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="1adb7-144">**Код профиля местонахождения:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-145">**Имя:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="1adb7-146">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1adb7-147">**Формат местонахождения:** *УПАКОВКА*</span><span class="sxs-lookup"><span data-stu-id="1adb7-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="1adb7-148">**Тип местоположения:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="1adb7-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="1adb7-149">**Использовать отслеживание грузомест:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="1adb7-150">**Разрешить смешанные номенклатуры:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="1adb7-151">**Разрешить смешанные статусы запасов:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="1adb7-152">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="1adb7-153">Ячейки</span><span class="sxs-lookup"><span data-stu-id="1adb7-153">Locations</span></span>

1. <span data-ttu-id="1adb7-154">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="1adb7-155">Снимите флажок **Создать контрольные разряды для местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="1adb7-156">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="1adb7-157">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="1adb7-158">**Местонахождение:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-159">**Код профиля местонахождения:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="1adb7-160">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="1adb7-161">Профили упаковки</span><span class="sxs-lookup"><span data-stu-id="1adb7-161">Packing profiles</span></span>

1. <span data-ttu-id="1adb7-162">Перейдите в раздел **Управление складом \> Настройка \> Упаковка \> Профили упаковки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="1adb7-163">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="1adb7-164">**Код профиля упаковки:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-165">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-166">**Политика упаковки контейнеров:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="1adb7-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="1adb7-167">**Режим кода контейнера:** *Авто*</span><span class="sxs-lookup"><span data-stu-id="1adb7-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="1adb7-168">**Тип контейнера:** *ПАЛЕТА 48X48*</span><span class="sxs-lookup"><span data-stu-id="1adb7-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="1adb7-169">**Автоматически создавать контейнер при закрытии контейнера:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="1adb7-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="1adb7-170">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="1adb7-171">Коды шагов волны</span><span class="sxs-lookup"><span data-stu-id="1adb7-171">Wave step codes</span></span>

<span data-ttu-id="1adb7-172">Если вы включили функцию *Код этапа волны для всей организации*, настройте следующий код.</span><span class="sxs-lookup"><span data-stu-id="1adb7-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="1adb7-173">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Коды этапов волны**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="1adb7-174">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="1adb7-175">**Код этапа волны:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-176">**Описание этапа волны:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-177">**Тип этапа волны:** *Шаблон сортировки*</span><span class="sxs-lookup"><span data-stu-id="1adb7-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="1adb7-178">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="1adb7-179">Шаблон исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="1adb7-179">Outbound sorting template</span></span>

<span data-ttu-id="1adb7-180">Шаблон сортировки определяет, создаются ли позиции сортировки, какие критерии используются и другие атрибуты процесса сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="1adb7-181">Выберите **Управление складом \> Настройка \> Упаковка \> Шаблон исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="1adb7-182">На панели операций выберите **Создать** для создания шаблона сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="1adb7-183">В заголовке нового шаблона задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="1adb7-184">**Код шаблона исходящей сортировки:** *Сортировка волны*</span><span class="sxs-lookup"><span data-stu-id="1adb7-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="1adb7-185">**Описание:** *Сортировка волны*</span><span class="sxs-lookup"><span data-stu-id="1adb7-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="1adb7-186">**Тип шаблона сортировки:** *Спрос волны*</span><span class="sxs-lookup"><span data-stu-id="1adb7-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="1adb7-187">Это поле определяет процесс, для которого используется шаблон сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="1adb7-188">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-188">The following values are available:</span></span>

        - <span data-ttu-id="1adb7-189">**Спрос волны** — шаблон сортировки используется для процесса *Поместить на стену*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="1adb7-190">Этот тип шаблона используется для обработки запасов прямо из волны, минуя станцию упаковки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="1adb7-191">Этот тип можно использовать только в том случае, если метод обработки волны **сортировка** включен в шаблон волны.</span><span class="sxs-lookup"><span data-stu-id="1adb7-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="1adb7-192">**Контейнер** — шаблон сортировки используется для процесса *Создание палеты после упаковки*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="1adb7-193">Этот тип шаблона используется для обработки контейнеров, которые закрыты на станции упаковки и должны быть отсортированы на палеты.</span><span class="sxs-lookup"><span data-stu-id="1adb7-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="1adb7-194">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="1adb7-195">**Местонахождение:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="1adb7-196">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1adb7-197">**Проверка сортировки:** *Скан позиции*</span><span class="sxs-lookup"><span data-stu-id="1adb7-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="1adb7-198">Это поле определяет проверку, требуемую при сортировке.</span><span class="sxs-lookup"><span data-stu-id="1adb7-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="1adb7-199">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-199">The following values are available:</span></span>

        - <span data-ttu-id="1adb7-200">Не допускается</span><span class="sxs-lookup"><span data-stu-id="1adb7-200">None</span></span>
        - <span data-ttu-id="1adb7-201">Скан грузоместа</span><span class="sxs-lookup"><span data-stu-id="1adb7-201">License plate scan</span></span>
        - <span data-ttu-id="1adb7-202">Скан позиции</span><span class="sxs-lookup"><span data-stu-id="1adb7-202">Position scan</span></span>

    - <span data-ttu-id="1adb7-203">**Создание работы при закрытии позиции:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="1adb7-204">Если для этого параметра задано значение *Да*, при закрытии позиции будет создаваться работа для перемещения запасов в конечное местоположение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="1adb7-205">Если для него задано значение *Нет*, запасы будут немедленно скомплектованы в заказ при закрытии позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="1adb7-206">**Назначение позиции:** *Вручную*</span><span class="sxs-lookup"><span data-stu-id="1adb7-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="1adb7-207">Это поле определяет тип назначения позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="1adb7-208">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-208">The following values are available:</span></span>

        - <span data-ttu-id="1adb7-209">**Вручную** — пользователь должен всегда указывать, в какую позицию запасов должна быть выполнена сортировка.</span><span class="sxs-lookup"><span data-stu-id="1adb7-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="1adb7-210">**Автоматически** — система автоматически направляет запасы в позицию, когда это возможно, на основе перерывов шаблона сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="1adb7-211">**Критерии назначения позиции сортировки:** *Использовать только пустую позицию*</span><span class="sxs-lookup"><span data-stu-id="1adb7-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="1adb7-212">Это поле определяет, будут ли запасы, уже имеющиеся в позициях сортировки, учитываться при назначении позиции для спроса.</span><span class="sxs-lookup"><span data-stu-id="1adb7-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="1adb7-213">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-213">The following values are available:</span></span>

        - <span data-ttu-id="1adb7-214">**Использовать только пустую позицию** — позиции, для которых уже имеются связанные с ними запасы, будут учтены</span><span class="sxs-lookup"><span data-stu-id="1adb7-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="1adb7-215">**Считать позицию пустой** — все запасы, уже находящиеся в этой позиции, не будут учитываться во время назначения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="1adb7-216">Будут использованы все доступные позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-216">All available positions will be used.</span></span>

    - <span data-ttu-id="1adb7-217">**Код этапа волны:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="1adb7-218">Если функция *Код этапа волны для всей организации* включена, код этапа волны *Сортировка* должен быть также настроен в кодах этапов волны.</span><span class="sxs-lookup"><span data-stu-id="1adb7-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="1adb7-219">**Автоматическое закрытие позиции сортировки:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="1adb7-220">Если для этого параметра задано значение *Да*, позиция сортировки автоматически закрывается после завершения всей работы, идущей в эту позицию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="1adb7-221">**Число позиций сортировки:** *3*</span><span class="sxs-lookup"><span data-stu-id="1adb7-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="1adb7-222">В этом поле определяется максимальное число позиций сортировки, которое будет создавать система.</span><span class="sxs-lookup"><span data-stu-id="1adb7-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="1adb7-223">**Префикс позиции сортировки:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="1adb7-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="1adb7-224">Это поле определяет префикс, который система назначает перед номером позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="1adb7-225">**Автоматическая упаковка позиции сортировки:** *Да*</span><span class="sxs-lookup"><span data-stu-id="1adb7-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="1adb7-226">Если для этого параметра задано значение *Да*, запасы на позиции сортировки будут упакованы в контейнер, когда позиция будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="1adb7-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="1adb7-227">**Код профиля упаковки:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="1adb7-228">Это поле определяет профиль упаковки, который будет использоваться при упаковке позиции сортировки в контейнер.</span><span class="sxs-lookup"><span data-stu-id="1adb7-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="1adb7-229">В области действий выберите **Изменить запрос**, чтобы указать критерии, которые используются для этого шаблона сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="1adb7-230">В диалоговом окне запрос на вкладке **Сортировка** выберите **Создать**, чтобы добавить строку, затем установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="1adb7-231">**Таблица:** *Сведения о загрузке*</span><span class="sxs-lookup"><span data-stu-id="1adb7-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="1adb7-232">**Производная таблица:** *Сведения о загрузке*</span><span class="sxs-lookup"><span data-stu-id="1adb7-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="1adb7-233">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="1adb7-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="1adb7-234">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="1adb7-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="1adb7-235">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-235">Select **OK**.</span></span>
1. <span data-ttu-id="1adb7-236">Может появиться следующее сообщение: "Группирование будет сброшено, продолжить?"</span><span class="sxs-lookup"><span data-stu-id="1adb7-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="1adb7-237">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-237">Select **Yes**.</span></span>

    <span data-ttu-id="1adb7-238">Становится доступной кнопка **Разбиения шаблона исходящей сортировки** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="1adb7-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="1adb7-239">На панели операций выберите **Разбиения шаблона исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="1adb7-240">Установите флажок **Поле для группировки**, чтобы сгруппировать по коду отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="1adb7-241">Этот параметр создаст одну позицию сортировки для каждой отгрузки, которая является контейнером в волне.</span><span class="sxs-lookup"><span data-stu-id="1adb7-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="1adb7-242">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="1adb7-243">Методы обработки волн</span><span class="sxs-lookup"><span data-stu-id="1adb7-243">Wave process methods</span></span>

1. <span data-ttu-id="1adb7-244">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="1adb7-245">В области операций выберите **Восстановить методы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="1adb7-246">Метод **сортировка** добавляется в список доступных методов, и для него выбирается тип шаблона волны *Отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="1adb7-247">Шаблоны волны</span><span class="sxs-lookup"><span data-stu-id="1adb7-247">Wave templates</span></span>

<span data-ttu-id="1adb7-248">Измените шаблон волны, который используется для сортировки спроса волны.</span><span class="sxs-lookup"><span data-stu-id="1adb7-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="1adb7-249">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="1adb7-250">В поле **Тип шаблона волн** выберите *Отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="1adb7-251">Выберите существующий шаблон **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="1adb7-252">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1adb7-253">На экспресс-вкладке **Общие** сделайте следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="1adb7-254">Установите для параметра **Обрабатывать волну перед запуском на склад** значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="1adb7-255">Установите для параметра **Назначить открытым волнам** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="1adb7-256">На экспресс-вкладке **Методы** настройте метод **сортировка**:</span><span class="sxs-lookup"><span data-stu-id="1adb7-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="1adb7-257">В сетке **Оставшиеся методы** выберите **сортировка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="1adb7-258">Выберите кнопку со стрелкой вправо, чтобы переместить метод **сортировка** в сетку **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="1adb7-259">В сетке **Выбранные методы** выберите **сортировка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="1adb7-260">Задайте в поле **Код этапа волны** значение *Сортировка*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="1adb7-261">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="1adb7-262">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="1adb7-262">Mobile device menu items</span></span>

1. <span data-ttu-id="1adb7-263">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1adb7-264">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1adb7-265">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="1adb7-266">**Имя пункта меню:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-267">**Заголовок:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="1adb7-268">**Режим:** *Косвенный*</span><span class="sxs-lookup"><span data-stu-id="1adb7-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="1adb7-269">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="1adb7-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="1adb7-270">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1adb7-271">**Код действия:** *Исходящая сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="1adb7-272">**Использовать руководство по процессу:** *Да* (значение по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1adb7-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="1adb7-273">**Код шаблона исходящей сортировки:** *Сортировка волны*</span><span class="sxs-lookup"><span data-stu-id="1adb7-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="1adb7-274">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="1adb7-275">Меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="1adb7-275">Mobile device menu</span></span>

1. <span data-ttu-id="1adb7-276">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="1adb7-277">В списке меню выберите **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="1adb7-278">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1adb7-279">В сетке **Доступные меню и пункты меню** найдите и выберите только что созданный пункт меню **Сортировка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="1adb7-280">Выберите кнопку со стрелкой вправо, чтобы переместить пункт **Сортировка** в сетке **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="1adb7-281">Таким образом, вы добавляете пункт меню в меню **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="1adb7-282">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="1adb7-283">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="1adb7-283">Location directives</span></span>

<span data-ttu-id="1adb7-284">Необходимо создать директивы местоположения, чтобы направлять работу, созданную после завершения сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="1adb7-285">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1adb7-286">В поле **Тип заказа на работу** выберите *Комплектация сортированных запасов*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="1adb7-287">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1adb7-288">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="1adb7-289">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="1adb7-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="1adb7-290">**Имя:** *Поместить к двери отсека*</span><span class="sxs-lookup"><span data-stu-id="1adb7-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="1adb7-291">На экспресс-вкладке **Директивы местоположения** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1adb7-292">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="1adb7-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1adb7-293">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="1adb7-293">**Site:** *6*</span></span>
    - <span data-ttu-id="1adb7-294">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="1adb7-295">**Код директивы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="1adb7-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="1adb7-296">**Несколько SKU:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="1adb7-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="1adb7-297">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="1adb7-298">На экспресс-вкладке **Строки** выберите **Создать**, затем установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="1adb7-299">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="1adb7-300">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="1adb7-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1adb7-301">**Количество "От":** *0*</span><span class="sxs-lookup"><span data-stu-id="1adb7-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="1adb7-302">**Количество "До":** *1000000*</span><span class="sxs-lookup"><span data-stu-id="1adb7-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="1adb7-303">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="1adb7-304">На экспресс-вкладке **Действия директивы местонахождения** выберите **Создать**, затем установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="1adb7-305">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="1adb7-306">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="1adb7-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1adb7-307">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="1adb7-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="1adb7-308">Выберите **Сохранить**, чтобы сделать доступной кнопку **Изменить запрос** на экспресс-вкладке **Действия директив местоположения**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="1adb7-309">На экспресс-вкладке **Действия директивы местоположения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="1adb7-310">В диалоговом окне запросов на вкладке **Диапазон** найдите строку, в которой поле **Поле** имеет значение *Местонахождение*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="1adb7-311">Задайте в поле **Критерии** для этой строки значение *Дверь отсека*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="1adb7-312">Выберите **ОК**, чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="1adb7-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="1adb7-313">Классы работы</span><span class="sxs-lookup"><span data-stu-id="1adb7-313">Work classes</span></span>

1. <span data-ttu-id="1adb7-314">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="1adb7-315">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1adb7-316">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="1adb7-317">**Код класса работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="1adb7-318">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="1adb7-319">**Тип заказа на работу:** *Комплектация сортированных запасов*</span><span class="sxs-lookup"><span data-stu-id="1adb7-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="1adb7-320">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="1adb7-321">Шаблоны работ</span><span class="sxs-lookup"><span data-stu-id="1adb7-321">Work templates</span></span>

1. <span data-ttu-id="1adb7-322">Перейдите в раздел **Управление складом \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1adb7-323">В поле **Тип заказа на работу** выберите *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="1adb7-324">В сетке выберите шаблон работы **62 Комплектация для упаковки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="1adb7-325">В панели операций выберите **Разрывы заголовка работы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="1adb7-326">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1adb7-327">В строке, где в поле **Имя поля** указано значение *Код отгрузки*, снимите флажок **Группировать по этому полю**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="1adb7-328">Выберите **Сохранить** и закройте диалоговое окно **Разрывы заголовка работы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="1adb7-329">В поле **Тип заказа на работу** выберите *Комплектация сортированных запасов*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="1adb7-330">Выберите **Создать** для создания шаблона работы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="1adb7-331">В разделе **Обзор** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="1adb7-332">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="1adb7-333">**Шаблон работы:** *Сортированная комплектация*</span><span class="sxs-lookup"><span data-stu-id="1adb7-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="1adb7-334">**Описание шаблон работы:** *Сортированная комплектация*</span><span class="sxs-lookup"><span data-stu-id="1adb7-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="1adb7-335">Выберите **Сохранить**, чтобы сделать доступным раздел **Сведения о шаблоне работы**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="1adb7-336">В разделе **Сведения о шаблоне работы** вы создадите две строки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="1adb7-337">Выберите **Создать**, затем задайте следующие значения для строки 1:</span><span class="sxs-lookup"><span data-stu-id="1adb7-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="1adb7-338">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="1adb7-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="1adb7-339">**Обязательно:** выбрано (= *Да*)</span><span class="sxs-lookup"><span data-stu-id="1adb7-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="1adb7-340">**Код класса работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="1adb7-341">Снова выберите **Создать**, затем задайте следующие значения для строки 2:</span><span class="sxs-lookup"><span data-stu-id="1adb7-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="1adb7-342">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="1adb7-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1adb7-343">**Обязательно:** выбрано (= *Да*)</span><span class="sxs-lookup"><span data-stu-id="1adb7-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="1adb7-344">**Код класса работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="1adb7-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="1adb7-345">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1adb7-346">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="1adb7-346">Example scenario</span></span>

<span data-ttu-id="1adb7-347">Этот сценарий имитирует ситуацию, в которой на складе хранятся небольшие номенклатуры в ячейках, и их необходимо упаковать в ящики до того, как они отгружаются, и когда функциональность станции упаковки не является действительно подходящей.</span><span class="sxs-lookup"><span data-stu-id="1adb7-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="1adb7-348">Работники могут скомплектовать заказы для нескольких клиентов и разных адресов одновременно, чтобы увеличить скорость комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="1adb7-349">После завершения комплектации работники прибывают на место сортировки, где подобранные номенклатуры могут быть отсортированы по соответствующим коробкам на основе требуемых критериев.</span><span class="sxs-lookup"><span data-stu-id="1adb7-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="1adb7-350">В этом примере код отгрузки будет использоваться для определения нужной коробки, поскольку каждая отгрузка имеет свой адрес.</span><span class="sxs-lookup"><span data-stu-id="1adb7-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="1adb7-351">После того, как все номенклатуры из загрузки упаковываются и сортируются по отгрузке, коробки будут перемещены в промежуточную область и в конечном счете загружаются на грузовик.</span><span class="sxs-lookup"><span data-stu-id="1adb7-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="1adb7-352">Прежде чем начать создание сценария, убедитесь, что все стандартные функции склада правильно настроены для склада.</span><span class="sxs-lookup"><span data-stu-id="1adb7-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="1adb7-353">Для этой цели используется стандартный склад Contoso *62*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="1adb7-354">Стандартные конфигурации не были изменены, кроме описанных в настройке.</span><span class="sxs-lookup"><span data-stu-id="1adb7-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="1adb7-355">Создание спроса</span><span class="sxs-lookup"><span data-stu-id="1adb7-355">Create demand</span></span>

<span data-ttu-id="1adb7-356">Прежде чем можно будет продемонстрировать функциональность, необходимо создать некоторый спрос.</span><span class="sxs-lookup"><span data-stu-id="1adb7-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="1adb7-357">В этом сценарии для моделирования различных адресов доставки будут созданы три заказа на продажу для трех различных клиентов.</span><span class="sxs-lookup"><span data-stu-id="1adb7-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="1adb7-358">Таким образом будут созданы три отдельные отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="1adb7-359">Перед созданием заказов на продажу и отгрузок необходимо убедиться, что в местах комплектации достаточно запасов для всех номенклатур по всем заказам.</span><span class="sxs-lookup"><span data-stu-id="1adb7-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="1adb7-360">Просмотрите настройки директивы местонахождения, чтобы проверить местонахождения комплектации, которые используются для комплектации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="1adb7-361">Если необходимо скорректировать запасы, можно создать ручные перемещения, воспользуйтесь пополнением или используйте любой другой поток.</span><span class="sxs-lookup"><span data-stu-id="1adb7-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="1adb7-362">Затем зарезервируйте запасы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="1adb7-363">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1adb7-364">Выберите **Создать**, чтобы создать заказ на продажу для заказа 1.</span><span class="sxs-lookup"><span data-stu-id="1adb7-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="1adb7-365">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1adb7-366">**Клиент:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="1adb7-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="1adb7-367">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1adb7-368">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-368">Select **OK**.</span></span>
1. <span data-ttu-id="1adb7-369">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1adb7-370">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-370">Set the following values:</span></span>

    - <span data-ttu-id="1adb7-371">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1adb7-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1adb7-372">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="1adb7-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="1adb7-373">Выберите **Добавить строку**, чтобы добавить вторую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="1adb7-374">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1adb7-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="1adb7-375">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="1adb7-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="1adb7-376">Повторите следующие шаги для каждой строки продажи в заказе, чтобы зарезервировать для нее запасы:</span><span class="sxs-lookup"><span data-stu-id="1adb7-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="1adb7-377">На экспресс-вкладке **Строки заказа на продажу** в меню **Запасы** выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="1adb7-378">На странице **Резервирование** выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="1adb7-379">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-379">Select **Save**.</span></span>

1. <span data-ttu-id="1adb7-380">Выберите **Создать**, чтобы создать заказ на продажу для заказа 2.</span><span class="sxs-lookup"><span data-stu-id="1adb7-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="1adb7-381">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1adb7-382">**Клиент:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="1adb7-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="1adb7-383">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1adb7-384">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-384">Select **OK**.</span></span>
1. <span data-ttu-id="1adb7-385">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1adb7-386">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-386">Set the following values:</span></span>

    - <span data-ttu-id="1adb7-387">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1adb7-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1adb7-388">**Количество:** *7*</span><span class="sxs-lookup"><span data-stu-id="1adb7-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="1adb7-389">Выберите **Добавить строку**, чтобы добавить вторую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="1adb7-390">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1adb7-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="1adb7-391">**Количество:** *3*</span><span class="sxs-lookup"><span data-stu-id="1adb7-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="1adb7-392">Повторите следующие шаги для каждой строки продажи в заказе, чтобы зарезервировать для нее запасы:</span><span class="sxs-lookup"><span data-stu-id="1adb7-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="1adb7-393">На экспресс-вкладке **Строки заказа на продажу** в меню **Запасы** выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="1adb7-394">На странице **Резервирование** выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="1adb7-395">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-395">Select **Save**.</span></span>

1. <span data-ttu-id="1adb7-396">Выберите **Создать**, чтобы создать заказ на продажу для заказа 3.</span><span class="sxs-lookup"><span data-stu-id="1adb7-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="1adb7-397">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1adb7-398">**Клиент:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="1adb7-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="1adb7-399">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1adb7-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1adb7-400">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-400">Select **OK**.</span></span>
1. <span data-ttu-id="1adb7-401">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1adb7-402">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1adb7-402">Set the following values:</span></span>

    - <span data-ttu-id="1adb7-403">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1adb7-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1adb7-404">**Количество:** *8*</span><span class="sxs-lookup"><span data-stu-id="1adb7-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="1adb7-405">Выполните следующие шаги, чтобы резервировать запасы для строки продажи:</span><span class="sxs-lookup"><span data-stu-id="1adb7-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="1adb7-406">На экспресс-вкладке **Строки заказа на продажу** в меню **Запасы** выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="1adb7-407">На странице **Резервирование** выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="1adb7-408">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-408">Select **Save**.</span></span>

<span data-ttu-id="1adb7-409">Выполните следующую процедуру, чтобы выпустить на склад каждый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="1adb7-410">Будут созданы три различных отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-410">Three different shipments will be created.</span></span> <span data-ttu-id="1adb7-411">Затем вы добавите все три отгрузки в одну новую волну.</span><span class="sxs-lookup"><span data-stu-id="1adb7-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="1adb7-412">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1adb7-413">В сетке выберите первый заказ на продажу, созданный вами.</span><span class="sxs-lookup"><span data-stu-id="1adb7-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="1adb7-414">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1adb7-415">Вы получаете информационное сообщение, которое показывает код волны и код отгрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="1adb7-416">Повторите предыдущие шаги для выпуска заказов на продажу 2 и 3 на склад.</span><span class="sxs-lookup"><span data-stu-id="1adb7-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="1adb7-417">Обратите внимание, что полученное информационное сообщение указывает на то, что отгрузка была добавлена в волну, созданная при выпуске заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="1adb7-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="1adb7-418">Перейдите в раздел **Управление складом \> Исходящие волны \> Волны отгрузок \> Все волны**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="1adb7-419">Выберите код волны, который был создан из выпуска заказов на продажу, чтобы открыть страницу **Волны**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="1adb7-420">На этой странице отображаются сведения о волне.</span><span class="sxs-lookup"><span data-stu-id="1adb7-420">This page shows the wave details.</span></span> <span data-ttu-id="1adb7-421">На экспресс-вкладке **Строки волны** отображаются созданные отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="1adb7-422">Теперь необходимо создать работу, чтобы переместить номенклатуры из ячеек комплектации в местоположение для сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="1adb7-423">В области панели операций выберите **Обработать**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="1adb7-424">Во время обработки волны метод сортировки использует шаблон сортировки для назначения запасов позициям сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="1adb7-425">Когда обработка волны завершена, вы получите информационное сообщение, сообщающее, что волна разнесена и работа была создана.</span><span class="sxs-lookup"><span data-stu-id="1adb7-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="1adb7-426">В области действий на вкладке **Волна** в группе **Связанные сведения** выберите **Работа** для просмотра созданной работы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="1adb7-427">Запишите код работы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="1adb7-428">Перейдите в раздел **Управление складом \> Упаковка и контейнеризация \> Назначение позиций исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="1adb7-429">В левом столбце можно просмотреть позицию исходящей сортировки, которая была создана для каждой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="1adb7-430">На экспресс-вкладке **Критерии позиции сортировки** можно просмотреть код отгрузки для этой позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="1adb7-431">Один код работы был создан, чтобы переместить запасы из местонахождений комплектации в местонахождение сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="1adb7-432">Для выполнения работы потребуется код работы, который был создан во время обработки волны.</span><span class="sxs-lookup"><span data-stu-id="1adb7-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="1adb7-433">Комплектация заказа на продажу в местонахождение сортировки</span><span class="sxs-lookup"><span data-stu-id="1adb7-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="1adb7-434">Выполните вход в мобильное приложение как работник на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="1adb7-435">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="1adb7-436">В меню **Исходящее** выберите **Комплектация продаж**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="1adb7-437">Выберите поле **Код**, затем введите код работы из обработки волны.</span><span class="sxs-lookup"><span data-stu-id="1adb7-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="1adb7-438">Подтвердите ввод.</span><span class="sxs-lookup"><span data-stu-id="1adb7-438">Confirm your entry.</span></span>

    <span data-ttu-id="1adb7-439">Далее будет предложено ввести конечное грузоместо (LP).</span><span class="sxs-lookup"><span data-stu-id="1adb7-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="1adb7-440">Обратите внимание на то, что строка 1 из заказа на продажу 1 должна быть скомплектована и добавлена на конечное грузоместо.</span><span class="sxs-lookup"><span data-stu-id="1adb7-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="1adb7-441">Отображаются код номенклатуры, количество, описание номенклатуры и местоположение комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="1adb7-442">В поле **Целевое грузоместо** введите код грузоместа.</span><span class="sxs-lookup"><span data-stu-id="1adb7-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="1adb7-443">Вы скомплектуете все строки, созданные из обработанной волны, на одно и то же конечное грузоместо.</span><span class="sxs-lookup"><span data-stu-id="1adb7-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="1adb7-444">Подтвердите ввод.</span><span class="sxs-lookup"><span data-stu-id="1adb7-444">Confirm your entry.</span></span>

    <span data-ttu-id="1adb7-445">Мобильное приложение теперь представляет серию страниц **Комплектация**, указывающую на место комплектации, и на номенклатуру и количество, которое необходимо скомплектовать.</span><span class="sxs-lookup"><span data-stu-id="1adb7-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="1adb7-446">После того как подобранная номенклатура добавлена на грузоместо, можно подтвердить работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="1adb7-447">Последней страницей будет работа по размещению скомплектованных номенклатур в местоположение сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="1adb7-448">Подтвердите первую работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="1adb7-449">Будет показана следующая работа комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-449">The next pick work is shown.</span></span> <span data-ttu-id="1adb7-450">Подтвердите комплектацию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-450">Confirm the pick.</span></span>
1. <span data-ttu-id="1adb7-451">Продолжите подтверждение оставшейся работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1adb7-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="1adb7-452">Последним шагом является завершение работы размещения.</span><span class="sxs-lookup"><span data-stu-id="1adb7-452">The last step is to complete the put work.</span></span> <span data-ttu-id="1adb7-453">Подтвердите размещение в местоположении сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="1adb7-454">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="1adb7-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="1adb7-455">Выйдите из пункта **Комплектация продаж** в мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="1adb7-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="1adb7-456">Сортировка/размещение на стене</span><span class="sxs-lookup"><span data-stu-id="1adb7-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="1adb7-457">После того, как все запасы будут помещены в местонахождение сортировки, они должны быть отсортированы в правильной позиции сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="1adb7-458">Войдите в мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="1adb7-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="1adb7-459">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="1adb7-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="1adb7-460">В меню **Исходящие** выберите **Сортировка** для начала сортировки номенклатур.</span><span class="sxs-lookup"><span data-stu-id="1adb7-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="1adb7-461">В поле **Грузоместо/контейнер** введите целевое грузоместо для работы скомплектованного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="1adb7-462">Подтвердите ввод.</span><span class="sxs-lookup"><span data-stu-id="1adb7-462">Confirm your entry.</span></span>
1. <span data-ttu-id="1adb7-463">Ввод код номенклатуры для сортировки в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="1adb7-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="1adb7-464">Система определяет первую позицию сортировки, которая должна отображаться.</span><span class="sxs-lookup"><span data-stu-id="1adb7-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="1adb7-465">Подтвердите позицию сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="1adb7-466">Вам будет предложено назначить грузоместо для позиции сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="1adb7-467">Выберите поле **Грузоместо**, введите номер грузоместа, затем подтвердите ввод.</span><span class="sxs-lookup"><span data-stu-id="1adb7-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="1adb7-468">Поскольку позиция сортировки связана с кодом отгрузки, отобранные номенклатуры будут отсортированы в грузоместо, относящееся к исходящей отгрузке и заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="1adb7-469">На следующей странице отображается код номенклатуры, количество, код позиции сортировки и коды грузоместа "из" (комплектация) и "в" (сортировка).</span><span class="sxs-lookup"><span data-stu-id="1adb7-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="1adb7-470">Сведения на этой странице дают указание отсортировать указанную номенклатуру и количества из грузоместа комплектации в грузоместо сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="1adb7-471">Подтвердите позицию сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="1adb7-472">Отсортируйте номенклатуры в первой позиции сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="1adb7-473">После завершения процедуры система направляет вас к следующей позиции сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="1adb7-474">Повторите эту процедуру для всех скомплектованных строк в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="1adb7-475">Этот процесс следует использовать также при наличии нескольких строк комплектации, имеющих одинаковый код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1adb7-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="1adb7-476">При повторном выполнении этого процесса для всех номенклатур система оценивает критерии из следующей отсканированной номенклатуры (строка работы) и определяет, в какую позицию сортировки ее следует поместить.</span><span class="sxs-lookup"><span data-stu-id="1adb7-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="1adb7-477">Вы автоматически направляетесь, чтобы поместить номенклатуру в нужную позицию сортировки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="1adb7-478">В зависимости от настройки подтверждения вы также направляетесь для подтверждение этого действия, вводя номер позиции или код грузоместа.</span><span class="sxs-lookup"><span data-stu-id="1adb7-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1adb7-479">Если автоматическая сортировка включена, переопределение вручную недоступно.</span><span class="sxs-lookup"><span data-stu-id="1adb7-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="1adb7-480">После завершения в Microsoft Dynamics 365 Supply Chain Management откройте страницу **Назначение позиций исходящей сортировки** для просмотра статуса позиций.</span><span class="sxs-lookup"><span data-stu-id="1adb7-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="1adb7-481">Если позиции закрываются автоматически, выберите **Показать закрытые**, чтобы отобразить закрытые позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="1adb7-482">Обратите внимание, что проводки позиции сортировки отображаются.</span><span class="sxs-lookup"><span data-stu-id="1adb7-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="1adb7-483">Отображаются номенклатура и количество, которые были обработаны по данной позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="1adb7-484">При настройке шаблона исходящей сортировки вы задали для параметра **Автоматическое закрытие позиции сортировки** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="1adb7-485">Таким образом, позиция автоматически закрывается после того, как в нее помещаются последние ожидаемые запасы.</span><span class="sxs-lookup"><span data-stu-id="1adb7-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="1adb7-486">Позиции сортировки имеют статус **Закрыто**, и работа была создана для перемещения отсортированных складских запасов в местонахождение *Дверь отсека*.</span><span class="sxs-lookup"><span data-stu-id="1adb7-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="1adb7-487">Выполните работу комплектации сортированных запасов, чтобы переместить запасы в место отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="1adb7-488">Когда запасы готовы, подтвердите их для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="1adb7-489">Для правильной обработки работы комплектации сортированных запасов пункт меню мобильного устройства с кодом класса работы, в котором в поле **Тип заказа на работу** настроено значение *Комплектация сортированных запасов*, следует использовать для процесса перемещения и загрузки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="1adb7-490">Закрытие позиции вручную (необязательно)</span><span class="sxs-lookup"><span data-stu-id="1adb7-490">Manually close a position (optional)</span></span>

<span data-ttu-id="1adb7-491">Если позиции сортировки должны быть закрыты вручную, параметр **Автоматическое закрытие позиции сортировки** для шаблона исходящей сортировки должен иметь значение *Нет*, и закрытие должно быть выполнено до того, как запасы могут быть перемещены в область двери отсека.</span><span class="sxs-lookup"><span data-stu-id="1adb7-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="1adb7-492">Позиции могут быть закрыты различными способами:</span><span class="sxs-lookup"><span data-stu-id="1adb7-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="1adb7-493">Через приложение склада:</span><span class="sxs-lookup"><span data-stu-id="1adb7-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="1adb7-494">Пользователь может отсканировать одну из номенклатур, уже расположенных в данной позиции, затем нажать кнопку **Закрыть**, чтобы закрыть эту позицию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="1adb7-495">Если пользователь сканирует контейнер, который уже отсортированный контейнер, выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1adb7-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="1adb7-496">Однако пользователь все равно может продолжать закрытие этой позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="1adb7-497">На странице **Назначения позиций исходящей сортировки** в Microsoft Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="1adb7-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="1adb7-498">Пользователь может выбрать запись позиции исходящей сортировки, затем выбрать **Закрыть позицию** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="1adb7-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="1adb7-499">Советы</span><span class="sxs-lookup"><span data-stu-id="1adb7-499">Tips</span></span>

- <span data-ttu-id="1adb7-500">Номенклатуры не могут быть перемещены между позициями после того, как они были назначены для одной позиции.</span><span class="sxs-lookup"><span data-stu-id="1adb7-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="1adb7-501">Система оценивает количество каждой номенклатуры, которое должно попасть в определенную позицию.</span><span class="sxs-lookup"><span data-stu-id="1adb7-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="1adb7-502">Шаблон сортировки можно настроить для автоматического создания контейнеров, когда позиции закрываются.</span><span class="sxs-lookup"><span data-stu-id="1adb7-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="1adb7-503">Этот подход создаст структуру кода стандартного контейнера, которая базируется на указанном профиле упаковки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1adb7-504">После создания работы по перемещению из местоположения сортировки вы не должны отменять работу.</span><span class="sxs-lookup"><span data-stu-id="1adb7-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="1adb7-505">В противном случае позиция и контейнеры в ней будут удалены из системы и недоступны для дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="1adb7-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="1adb7-506">Запасы также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="1adb7-506">The inventory will also be removed.</span></span>