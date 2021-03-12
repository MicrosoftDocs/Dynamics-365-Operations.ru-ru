---
title: Кластеры размещения
description: Кластеры размещения предлагают способ скомплектовать несколько грузомест в одно и то же время, а затем взять их для размещения в различных местах. Они могут быть очень полезны для предприятий розничной торговли, где грузоместа обычно не являются заполненными палетами запасов.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996206"
---
# <a name="putaway-clusters"></a><span data-ttu-id="ae3f9-104">Кластеры размещения</span><span class="sxs-lookup"><span data-stu-id="ae3f9-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae3f9-105">Кластеры размещения предлагают способ скомплектовать несколько грузомест в одно и то же время, а затем взять их для размещения в различных местах.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="ae3f9-106">Данный процесс часто называется *доставкой сборных грузов*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="ae3f9-107">Кластеры размещения могут быть очень полезны для предприятий розничной торговли, где грузоместа обычно не являются заполненными палетами запасов.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="ae3f9-108">Включение функции кластеров размещения</span><span class="sxs-lookup"><span data-stu-id="ae3f9-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="ae3f9-109">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ae3f9-110">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ae3f9-111">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ae3f9-112">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ae3f9-113">**Имя компонента:** *Функция кластеров размещения*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="ae3f9-114">Настройка примера сценария</span><span class="sxs-lookup"><span data-stu-id="ae3f9-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="ae3f9-115">Профили кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-115">Cluster profiles</span></span>

<span data-ttu-id="ae3f9-116">Профиль кластера размещения определяет, куда будет идти номенклатура, на основе местоположения, назначенного номенклатуре в момент приемки.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="ae3f9-117">Если необходимы разные кластеры, требуется создать разные кластеры размещения, по одному для каждого пункта меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="ae3f9-118">Перейдите **Управление складом \> Настройка \> Мобильное устройство \> Профили кластера**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="ae3f9-119">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ae3f9-120">В представлении **Заголовок** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-121">**Код профиля кластера размещения:** *Кластер размещения*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="ae3f9-122">**Имя кода профиля кластера размещения:** *Кластер размещения*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="ae3f9-123">**Тип кластера:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="ae3f9-124">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="ae3f9-125">Выберите **Сохранить**, чтобы сделать доступными обязательные поля на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="ae3f9-126">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-127">**Время назначения кластера:** *По приходу*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="ae3f9-128">Это поле определяет, должен ли кластер размещения быть назначен немедленно при получении запасов или он должен быть отсортирован позже.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="ae3f9-129">**Правило назначения кластеров:** *Вручную*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="ae3f9-130">Это поле определяет, должно ли назначение кластера определяться системой автоматически или вручную пользователем.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="ae3f9-131">**Код директивы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="ae3f9-132">**Поиск кластера размещения:** *Приемка*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="ae3f9-133">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-133">The following values are available:</span></span>

        - <span data-ttu-id="ae3f9-134">**Приемка** — местоположение будет найдено сразу в ходе приемки.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="ae3f9-135">**Закрытие кластера** — местоположение находится при закрытии кластера.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="ae3f9-136">**По выбора пользователя** — местоположение находится, когда грузоместо выбирается из кластера для размещения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="ae3f9-137">В этом случае местоположение не указывается при создании работы размещения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="ae3f9-138">Во время самого размещения пользователь должен отсканировать этикетку грузоместа или код работы, чтобы начать шаг размещения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="ae3f9-139">Затем система находит местоположение размещения снова и сообщает пользователю, куда поместить скомплектованное количество.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="ae3f9-140">**Кластер размещения для каждого пользователя:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="ae3f9-141">Это поле определяет, должен ли каждый кластер быть уникальным для каждого пользователя при автоматическом назначении кластеров.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="ae3f9-142">Оно доступно только в том случае, если в поле **Правило назначения кластеров** установлено значение *Автоматически*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="ae3f9-143">**Ограничение единиц:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="ae3f9-144">Это поле определяет единицу измерения, которая должна быть получена, чтобы профиль был действительным.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="ae3f9-145">Если оставить его пустым, будут действительны все единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="ae3f9-146">**Разрыв в единицах работы:** *Индивидуальный*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="ae3f9-147">Это поле определяет, следует ли консолидировать все запасы (используя код кластера и грузоместо) на одном грузоместе, когда кластер закрывается, и должен ли он размещаться как одно грузоместо или отдельно на грузоместах, которые были получены.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="ae3f9-148">Это поле недоступно, если для поля **Поиск кластера размещения** выбрано значение *Приход*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="ae3f9-149">**Кластер сохраняется как родительское грузоместо:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="ae3f9-150">Если для этого параметра установлено значение *Да*, то после завершения шага размещения код кластера станет родительским грузоместом, а все номенклатуры с кодом кластера будут связаны с родительским грузоместом.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="ae3f9-151">На экспресс-вкладке **Сортировка кластера** можно определить критерий сортировки размещения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="ae3f9-152">Выберите **Создать** на панели инструментов, чтобы добавить строку, затем установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="ae3f9-153">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="ae3f9-154">**Имя поля:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="ae3f9-155">Это поле определяет поле, которое данная строка должна использовать в качестве критерия сортировки.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="ae3f9-156">**Сортировка:** *По возрастанию*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="ae3f9-157">Это поле определяет, должна ли сортировка производиться в восходящем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="ae3f9-158">На экспресс-вкладке **Шаблон работы кластера** выберите **Создать** на панели инструментов, чтобы добавить строку, затем установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="ae3f9-159">**Тип заказа на работу:** *Заказы на покупку*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="ae3f9-160">**Шаблон работы:** *61 PO Прямая*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="ae3f9-161">На панели операций выберите **Сохранить**, затем выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="ae3f9-162">В диалоговом окне **Кластер размещения** на вкладке **Диапазон** выберите **Добавить**, чтобы добавить вторую строку в запрос.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="ae3f9-163">Затем обновите строки запроса, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="ae3f9-164">Таблица</span><span class="sxs-lookup"><span data-stu-id="ae3f9-164">Table</span></span> | <span data-ttu-id="ae3f9-165">Производная таблица</span><span class="sxs-lookup"><span data-stu-id="ae3f9-165">Derived table</span></span> | <span data-ttu-id="ae3f9-166">Поле</span><span class="sxs-lookup"><span data-stu-id="ae3f9-166">Field</span></span> | <span data-ttu-id="ae3f9-167">Критерии</span><span class="sxs-lookup"><span data-stu-id="ae3f9-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="ae3f9-168">Действует</span><span class="sxs-lookup"><span data-stu-id="ae3f9-168">Work</span></span> | <span data-ttu-id="ae3f9-169">Действует</span><span class="sxs-lookup"><span data-stu-id="ae3f9-169">Work</span></span> | <span data-ttu-id="ae3f9-170">Склад</span><span class="sxs-lookup"><span data-stu-id="ae3f9-170">Warehouse</span></span> | <span data-ttu-id="ae3f9-171">*61*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-171">*61*</span></span> |
    | <span data-ttu-id="ae3f9-172">Действует</span><span class="sxs-lookup"><span data-stu-id="ae3f9-172">Work</span></span> | <span data-ttu-id="ae3f9-173">Действует</span><span class="sxs-lookup"><span data-stu-id="ae3f9-173">Work</span></span> | <span data-ttu-id="ae3f9-174">Код работы</span><span class="sxs-lookup"><span data-stu-id="ae3f9-174">Work ID</span></span> | <span data-ttu-id="ae3f9-175">Оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="ae3f9-176">Выберите **OK**, чтобы сохранить запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="ae3f9-177">На панели операций выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae3f9-178">Поля в профиле кластера, которые будут недоступными, если для параметра **Формировать код кластера** задано значение *Да*, недоступны и не будут учитываться при использовании этой функции.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="ae3f9-179">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="ae3f9-179">Mobile device menu items</span></span>

<span data-ttu-id="ae3f9-180">Для этой функции доступны два новых пункта меню для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="ae3f9-181">Пункт меню **Получение и сортировка кластера** используется для сортировки полученных запасов в кластер размещения в ходе приемки.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="ae3f9-182">Пункт меню **Кластер размещения** используется для размещения кластера после того, как он был назначен.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="ae3f9-183">Получение и сортировка кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-183">Receive and sort cluster</span></span>

<span data-ttu-id="ae3f9-184">Создайте новый пункт меню мобильного устройства для получения запасов и сортировки в кластер.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="ae3f9-185">Этот пункт меню создает входящую работу после получения запасов, которая указывает на то, что пункт меню приемки будет использоваться для размещения кластеров.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="ae3f9-186">Пункт меню **Получение и сортировка кластера** может использоваться со следующими пунктами меню получения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="ae3f9-187">Получение строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="ae3f9-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="ae3f9-188">Получение номенклатуры заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="ae3f9-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="ae3f9-189">Загрузить получение номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-189">Load item receiving</span></span>

1. <span data-ttu-id="ae3f9-190">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ae3f9-191">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ae3f9-192">В представлении **Заголовок** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-193">**Имя пункта меню:** *Получение и сортировка кластера*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="ae3f9-194">**Название:** *Получение и сортировка кластера*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="ae3f9-195">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ae3f9-196">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="ae3f9-197">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-198">**Процесс создания работы:** *Получение номенклатуры заказа на покупку*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="ae3f9-199">**Создать грузоместо:** *Да*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="ae3f9-200">**Назначение кластера размещения:** *Да*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="ae3f9-201">Параметр **Назначение кластера размещения** доступен только для одношагового действия *Процесс создания работы* для получения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="ae3f9-202">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="ae3f9-203">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="ae3f9-204">Размещение кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-204">Cluster putaway</span></span>

<span data-ttu-id="ae3f9-205">Создайте новый пункт меню мобильного устройства для размещения кластера после того, как он был назначен.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="ae3f9-206">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ae3f9-207">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ae3f9-208">В представлении **Заголовок** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-209">**Имя пункта меню:** *Размещение кластера*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="ae3f9-210">**Заголовок:** *Размещение кластера*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="ae3f9-211">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ae3f9-212">**Использовать существующую работу:** *Да*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="ae3f9-213">На экспресс-вкладке **Общие** задайте в поле **Кем управляется** значение *Размещение кластера*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="ae3f9-214">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="ae3f9-215">На экспресс-вкладке **Классы работ** настройте допустимый класс работы для этого пункта меню мобильного устройства:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="ae3f9-216">**Код класса работы:** *Покупка*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="ae3f9-217">**Тип заказа на работу:** *Заказы на покупку*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="ae3f9-218">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="ae3f9-219">Меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="ae3f9-219">Mobile device menu</span></span>

<span data-ttu-id="ae3f9-220">Добавьте только что созданные пункты меню во входящее меню мобильного приложения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="ae3f9-221">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ae3f9-222">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ae3f9-223">В списке меню выберите **Входящие**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="ae3f9-224">В списке **Доступные меню и пункты меню** найдите и выберите **Получение и сортировка кластера**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="ae3f9-225">Нажмите кнопку со стрелкой вправо, чтобы переместить выбранный пункт меню в список **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="ae3f9-226">Используйте кнопки со стрелкой вверх или вниз для перемещения пункта меню в нужную позицию в меню.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="ae3f9-227">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ae3f9-228">Повторите шаги с 4 по 7, чтобы добавить остальные пункты меню:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="ae3f9-229">Назначение кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-229">Assign cluster</span></span>
    - <span data-ttu-id="ae3f9-230">Размещение кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ae3f9-231">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="ae3f9-231">Example scenario</span></span>

<span data-ttu-id="ae3f9-232">Этот сценарий имитирует обработку кластера размещения.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="ae3f9-233">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="ae3f9-233">Create a purchase order</span></span>

1. <span data-ttu-id="ae3f9-234">Перейдите в раздел **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ae3f9-235">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ae3f9-236">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ae3f9-237">**Счет поставщика:** *1001*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="ae3f9-238">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ae3f9-239">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-239">Select **OK**.</span></span>

    <span data-ttu-id="ae3f9-240">Открывается страница **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="ae3f9-241">На странице **Все заказы на покупку** на экспресс-вкладке **Строки заказа на покупку** с помощью кнопки **Добавить строку** добавьте следующие строки:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="ae3f9-242">Строка 1 заказа на покупку:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="ae3f9-243">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ae3f9-244">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="ae3f9-245">Строка 2 заказа на покупку:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="ae3f9-246">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ae3f9-247">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="ae3f9-248">Строка 3 заказа на покупку:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="ae3f9-249">**Код номенклатуры:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="ae3f9-250">**Количество:** *30*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="ae3f9-251">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ae3f9-252">Запишите номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="ae3f9-253">Получение запасов и их размещение с мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="ae3f9-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="ae3f9-254">Получение и сортировка запасов в кластер</span><span class="sxs-lookup"><span data-stu-id="ae3f9-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="ae3f9-255">Выполните вход в приложение склада в качестве пользователя, который настроен для склада *61*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="ae3f9-256">В главном меню выберите **Входящие**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="ae3f9-257">В меню **Входящие** выберите **Получить и сортировать кластер**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="ae3f9-258">В поле **PONUM** введите номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="ae3f9-259">Выберите **ОК** (кнопка с символом галочки).</span><span class="sxs-lookup"><span data-stu-id="ae3f9-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ae3f9-260">Выберите поле **Номенклатура**, введите номер номенклатуры *A0001* и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="ae3f9-261">Выберите поле **Кол-во**, введите *10* с помощью числовой панели, а затем нажмите кнопку с галочкой.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="ae3f9-262">На странице задачи **Кол-во** выберите **ОК** (кнопка с галочкой), чтобы подтвердить введенное количество.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="ae3f9-263">На странице задачи **Номенклатура** выберите **ОК**, чтобы подтвердить, что номенклатура *A0001* была введена.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="ae3f9-264">Выберите поле **Код кластера** и введите значение, чтобы назначить код для создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="ae3f9-265">Введенный здесь код будет использоваться при получении двух оставшихся номенклатур в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="ae3f9-266">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-266">Select **OK**.</span></span>

    <span data-ttu-id="ae3f9-267">Отображается страница задачи **Ponum** и отображается сообщение "Работа выполнена".</span><span class="sxs-lookup"><span data-stu-id="ae3f9-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="ae3f9-268">Номенклатура *A0001* теперь получена в местоположение *RECV* и назначена коду кластера, введенному на шаге 10.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="ae3f9-269">Повторите шаги с 4 по 11 для получения оставшихся двух номенклатур из заказа на покупку и назначьте их коду кластера:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="ae3f9-270">Количество *20* для номенклатуры *A0002*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="ae3f9-271">Количество *30* для номенклатуры *M9215*</span><span class="sxs-lookup"><span data-stu-id="ae3f9-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="ae3f9-272">Закрытие кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-272">Close the cluster</span></span>

<span data-ttu-id="ae3f9-273">Прежде чем номенклатуры в кластере можно будет разместить, кластер необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="ae3f9-274">В Supply Chain Management перейдите в раздел **Управление складом \> Работа \> Исходящие \> Кластеры работ**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="ae3f9-275">На странице **Кластеры работ** в разделе **Кластер работы** найдите в поле **Код кластера** код кластера, который был введен ранее.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="ae3f9-276">Если кластер не отображается, он может быть уже закрыт.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="ae3f9-277">Чтобы определить, был ли кластер закрыт, установите флажок **Показать закрытую работу** и выполните поиск кода кластера, который был введен ранее.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="ae3f9-278">Затем выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="ae3f9-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="ae3f9-279">Если кластер был закрыт, пропустите остальные шаги этой процедуры и перейдите к следующей процедуре, [Размещение кластера](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="ae3f9-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="ae3f9-280">Если кластер не был закрыт, выполните остальные шаги этой процедуры, чтобы вручную закрыть кластер.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="ae3f9-281">Затем переходите к следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="ae3f9-282">В разделе **Кластер работ** выберите код кластера, который был введен ранее.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="ae3f9-283">В области действий выберите **Закрыть кластер**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="ae3f9-284">После закрытия кластера он больше не отображается в разделе **Кластер работ** (если только не установлен флажок **Показывать закрытую работу**).</span><span class="sxs-lookup"><span data-stu-id="ae3f9-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="ae3f9-285">Размещение кластера</span><span class="sxs-lookup"><span data-stu-id="ae3f9-285">Put the cluster away</span></span>

1. <span data-ttu-id="ae3f9-286">Выполните вход в приложение склада в качестве пользователя, который настроен для склада *61*.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="ae3f9-287">В главном меню выберите **Входящие**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="ae3f9-288">В меню **Входящие** выберите **Разместить кластер**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="ae3f9-289">Выберите **Код кластера** и введите код кластера, который был введен ранее для закрытого кластера.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="ae3f9-290">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-290">Select **OK**.</span></span>

    <span data-ttu-id="ae3f9-291">Будет открыта страница **Размещение кластера: комплектация**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="ae3f9-292">Здесь отображается код кластера, местоположение комплектации, номенклатуры (значение *Несколько* будет отображаться)" и общее количество в кластере, которое необходимо скомплектовать.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="ae3f9-293">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-293">Select **OK**.</span></span>

    <span data-ttu-id="ae3f9-294">Будет открыта страница **Размещение кластера: размещение**.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="ae3f9-295">Инструкции **Разместить** идентифицируют код кластера, местоположение размещения, номенклатуры, общее количество и коды грузомест для номенклатур, полученных в кластере.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="ae3f9-296">Имеются стандартные параметры переопределения или прохождения этого шага.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="ae3f9-297">![Размещение кластера: страница размещения](media/Cluster_putaway-Put.png "Размещение кластера: страница размещения")</span><span class="sxs-lookup"><span data-stu-id="ae3f9-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="ae3f9-298">Выберите **ОК**, чтобы подтвердить размещение кластера.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="ae3f9-299">Отображается сообщение "Кластер завершен".</span><span class="sxs-lookup"><span data-stu-id="ae3f9-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="ae3f9-300">Примечания и советы</span><span class="sxs-lookup"><span data-stu-id="ae3f9-300">Notes and tips</span></span>

<span data-ttu-id="ae3f9-301">Для случаев, когда код кластера становится родительским грузоместом для вложенной палеты, позиция размещения автоматически назначается при сканировании кода кластера.</span><span class="sxs-lookup"><span data-stu-id="ae3f9-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="ae3f9-302">Дальнейшее сканирование грузоместа не требуется, даже если для создания грузоместа задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="ae3f9-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
