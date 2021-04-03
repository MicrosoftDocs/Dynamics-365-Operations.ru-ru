---
title: Плановый кросс-докинг
description: В этой теме описывается усовершенствованный плановый кросс-докинг, где количество запасов, необходимое для заказа, направляется прямо из приемки или создания в правильный дебаркадер отгрузки или промежуточную область. Все остальные запасы из входящего источника направляются в правильное место хранения через процесс обычного размещения.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556274"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="37ac5-104">Плановый кросс-докинг</span><span class="sxs-lookup"><span data-stu-id="37ac5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ac5-105">В этой теме описывается расширенный плановый кросс-докинг.</span><span class="sxs-lookup"><span data-stu-id="37ac5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="37ac5-106">Кросс-докинг — это складской процесс, где количество запасов, необходимое для заказа, направляется прямо из приемки или создания в правильный дебаркадер отгрузки или промежуточную область.</span><span class="sxs-lookup"><span data-stu-id="37ac5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="37ac5-107">Все остальные запасы из входящего источника направляются в правильное место хранения через процесс обычного размещения.</span><span class="sxs-lookup"><span data-stu-id="37ac5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="37ac5-108">Кросс-докинг позволяет сотрудникам пропускать входящее размещение и исходящую комплектацию запасов, уже помеченных для исходящего заказа.</span><span class="sxs-lookup"><span data-stu-id="37ac5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="37ac5-109">Таким образом, число случаев, когда запасы затрагиваются, уменьшается, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="37ac5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="37ac5-110">Кроме того, поскольку имеется меньше взаимодействия с системой, увеличивается экономия времени и места складирования на складе.</span><span class="sxs-lookup"><span data-stu-id="37ac5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="37ac5-111">Прежде чем можно будет выполнить кросс-докинг, пользователь должен настроить новый шаблон кросс-докинга, где указаны источник поставок и другие наборы требований для кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="37ac5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="37ac5-112">При создании исходящего заказа строка должна быть помечена для входящего заказа, который содержит ту же номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="37ac5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="37ac5-113">Во время получения входящего заказа настройка кросс-докинга автоматически определяет потребность в кросс-докинге и создает работу перемещения для требуемого количества на основе настройки директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="37ac5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="37ac5-114">При отмене работы кросс-докинга регистрация складских проводок **не** отменяется, даже если настройка для этой возможности включена в параметрах управления складом.</span><span class="sxs-lookup"><span data-stu-id="37ac5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="37ac5-115">Включение функций планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="37ac5-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="37ac5-116">Если ваша система еще не содержит функций, описанных в этом разделе, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="37ac5-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="37ac5-117">*Плановый кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="37ac5-118">*Шаблоны кросс-докинга с директивами мест хранения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="37ac5-119">Настройка</span><span class="sxs-lookup"><span data-stu-id="37ac5-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="37ac5-120">Повторное создание методов разноски загрузки</span><span class="sxs-lookup"><span data-stu-id="37ac5-120">Regenerate load posting methods</span></span>

<span data-ttu-id="37ac5-121">Плановый кросс-докинг реализован как метод разноски загрузки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="37ac5-122">После включения функции необходимо повторно создать методы.</span><span class="sxs-lookup"><span data-stu-id="37ac5-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="37ac5-123">Перейдите в раздел **Управление складом \> Настройка \> Методы разноски загрузки**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="37ac5-124">В области операций выберите **Восстановить методы**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="37ac5-125">После завершения повторного создания должен отобразиться метод со значение **Имя метода**, равным *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="37ac5-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="37ac5-127">Создание шаблона кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="37ac5-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="37ac5-128">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны кросс-докинга**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="37ac5-129">На панели операций выберите **Создать** для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="37ac5-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="37ac5-130">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="37ac5-131">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="37ac5-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="37ac5-132">Это поле определяет порядок, в котором оцениваются шаблоны.</span><span class="sxs-lookup"><span data-stu-id="37ac5-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="37ac5-133">**Код шаблона кросс-докинга:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="37ac5-134">**Описание:** *Склад 51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="37ac5-135">**Политика выпуска спроса:** *Перед получением поставки*</span><span class="sxs-lookup"><span data-stu-id="37ac5-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="37ac5-136">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="37ac5-137">Настройка на экспресс-вкладке **Планирование** управляет тем, как будет работать шаблон.</span><span class="sxs-lookup"><span data-stu-id="37ac5-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="37ac5-138">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-138">Set the following values:</span></span>

    - <span data-ttu-id="37ac5-139">**Требования к спросу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="37ac5-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="37ac5-140">Это поле определяет требования к запасам спроса.</span><span class="sxs-lookup"><span data-stu-id="37ac5-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="37ac5-141">Если спрос должен быть связан с поставками до выпуска, выберите *Маркировка*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="37ac5-142">Если спрос должен быть зарезервирован по заказам для поставок до выпуска, выберите *Резервирование заказа*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="37ac5-143">**Тип местонахождения:** *Местонахождения отгрузок*</span><span class="sxs-lookup"><span data-stu-id="37ac5-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="37ac5-144">Это поле определяет, должна ли работа кросс-докинга использовать местоположения промежуточного хранения/загрузки из отгрузки, или следует ли использовать директивы местоположения для поиска собственных местоположений промежуточного хранения/загрузки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="37ac5-145">**Шаблон работы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="37ac5-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="37ac5-146">Это поле определяет шаблон работы, который должен использоваться при создании работы по кросс-докингу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="37ac5-147">**Повторная проверка при поступлении поставок:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="37ac5-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="37ac5-148">Этот параметр определяет, должна ли поставка быть повторно проверена в ходе приемки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="37ac5-149">Если этот параметр имеет значение *Да*, проверяются как максимальный промежуток времени, так и диапазон дней истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="37ac5-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="37ac5-150">**Код директивы** Оставьте это поле пустым</span><span class="sxs-lookup"><span data-stu-id="37ac5-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="37ac5-151">Этот параметр позволяет системе использовать директивы местоположения, чтобы определить оптимальное местоположение для перемещения в него запасов кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="37ac5-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="37ac5-152">Настройку можно выполнить, назначив код директивы каждому соответствующему шаблону кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="37ac5-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="37ac5-153">Каждый код директивы определяет уникальную директиву местоположения.</span><span class="sxs-lookup"><span data-stu-id="37ac5-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="37ac5-154">**Проверка окна времени:** *Да*</span><span class="sxs-lookup"><span data-stu-id="37ac5-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="37ac5-155">Этот параметр определяет, следует ли оценивать максимальное окно времени при выборе источника поставки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="37ac5-156">Если для этого параметра установлено значение *Да*, становятся доступны поля, которые относятся к максимальному и минимальному окну времени.</span><span class="sxs-lookup"><span data-stu-id="37ac5-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="37ac5-157">**Максимальное временное окно:** *5*</span><span class="sxs-lookup"><span data-stu-id="37ac5-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="37ac5-158">Это поле определяет максимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="37ac5-159">**Единица максимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="37ac5-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="37ac5-160">**Минимальное временное окно:** *0*</span><span class="sxs-lookup"><span data-stu-id="37ac5-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="37ac5-161">Это поле определяет минимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="37ac5-162">**Единица минимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="37ac5-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="37ac5-163">**Диапазон истечения срока действия в днях:** *0*</span><span class="sxs-lookup"><span data-stu-id="37ac5-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="37ac5-164">*Критерий первоочередного отпуска товаров с ближайшим сроком годности (FEFO):* в этом поле определяется максимальное число дней между ближайшей датой окончания срока годности партии, которая в настоящее время находится на складе, и полученной партией.</span><span class="sxs-lookup"><span data-stu-id="37ac5-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="37ac5-165">На экспресс-вкладке **Источники поставок** указываются типы поставок, которые действительны для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="37ac5-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="37ac5-166">Выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="37ac5-167">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="37ac5-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="37ac5-168">**Источник поставок:** *Заказ на покупку*</span><span class="sxs-lookup"><span data-stu-id="37ac5-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="37ac5-169">Создание класса работ</span><span class="sxs-lookup"><span data-stu-id="37ac5-169">Create a work class</span></span>

1. <span data-ttu-id="37ac5-170">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="37ac5-171">На панели операций выберите **Создать** для создания класса работ.</span><span class="sxs-lookup"><span data-stu-id="37ac5-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="37ac5-172">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-172">Set the following values:</span></span>

    - <span data-ttu-id="37ac5-173">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="37ac5-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="37ac5-174">**Описание:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="37ac5-175">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="37ac5-176">Создание шаблона работы</span><span class="sxs-lookup"><span data-stu-id="37ac5-176">Create a work template</span></span>

1. <span data-ttu-id="37ac5-177">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="37ac5-178">Задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="37ac5-179">На панели операций выберите **Создать**, чтобы добавить строку на вкладку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="37ac5-180">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-181">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="37ac5-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="37ac5-182">**Шаблон работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="37ac5-183">**Описание шаблона работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="37ac5-184">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Сведения о шаблоне работы**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="37ac5-185">На экспресс-вкладке **Сведения о шаблоне работы** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="37ac5-186">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-187">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="37ac5-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="37ac5-188">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="37ac5-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="37ac5-189">Выберите **Создать**, чтобы добавить еще одну строку, и установите следующие значения в ней:</span><span class="sxs-lookup"><span data-stu-id="37ac5-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="37ac5-190">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="37ac5-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="37ac5-191">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="37ac5-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="37ac5-192">Выберите **Сохранить** и убедитесь, что установлен флажок **Допустимый** для шаблона *51 Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="37ac5-193">Коды классов работ для типов работ *Комплектация* и *Размещение* должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="37ac5-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="37ac5-194">Создание директив местонахождения</span><span class="sxs-lookup"><span data-stu-id="37ac5-194">Create location directives</span></span>

1. <span data-ttu-id="37ac5-195">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="37ac5-196">В левой панели задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="37ac5-197">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="37ac5-198">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="37ac5-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="37ac5-199">**Имя:** *51 кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="37ac5-200">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="37ac5-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="37ac5-201">**Сайт:** *5*</span><span class="sxs-lookup"><span data-stu-id="37ac5-201">**Site:** *5*</span></span>
    - <span data-ttu-id="37ac5-202">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="37ac5-203">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="37ac5-204">На экспресс-вкладке **Строки** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="37ac5-205">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-206">**Количество "От":** *1*</span><span class="sxs-lookup"><span data-stu-id="37ac5-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="37ac5-207">**Количество "До":** *1000000*</span><span class="sxs-lookup"><span data-stu-id="37ac5-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="37ac5-208">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="37ac5-209">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="37ac5-210">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-211">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="37ac5-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="37ac5-212">**Использование фиксированного местоположения:** *Фиксированные и нефиксированные местонахождения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="37ac5-213">Выберите **Сохранить**, чтобы сделать доступной кнопку **Изменить запрос** на панели инструментов **Действия директив местоположения**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="37ac5-214">Выберите **Изменить запрос**, чтобы открыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="37ac5-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="37ac5-215">На вкладке **Диапазон** убедитесь, что настроены следующие две строки:</span><span class="sxs-lookup"><span data-stu-id="37ac5-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="37ac5-216">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="37ac5-216">Line 1:</span></span>

        - <span data-ttu-id="37ac5-217">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="37ac5-218">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="37ac5-219">**Поле:** *Склад*</span><span class="sxs-lookup"><span data-stu-id="37ac5-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="37ac5-220">**Критерий:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="37ac5-221">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="37ac5-221">Line 2:</span></span>

        - <span data-ttu-id="37ac5-222">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="37ac5-223">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="37ac5-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="37ac5-224">**Поле:** *Местонахождение*</span><span class="sxs-lookup"><span data-stu-id="37ac5-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="37ac5-225">**Критерий:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="37ac5-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="37ac5-226">Выберите **ОК**, чтобы закрыть редактор запроса.</span><span class="sxs-lookup"><span data-stu-id="37ac5-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="37ac5-227">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="37ac5-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="37ac5-228">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="37ac5-229">В списке пунктов меню в левой области выберите вариант **Размещение покупки**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="37ac5-230">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-230">Select **Edit**.</span></span>
1. <span data-ttu-id="37ac5-231">На экспресс-вкладке **Классы работ** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="37ac5-232">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-233">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="37ac5-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="37ac5-234">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="37ac5-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="37ac5-235">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="37ac5-236">Сценарий</span><span class="sxs-lookup"><span data-stu-id="37ac5-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="37ac5-237">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="37ac5-237">Create a purchase order</span></span>

<span data-ttu-id="37ac5-238">Выполните следующие действия, чтобы создать заказ на покупку в качестве источника поставки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="37ac5-239">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="37ac5-240">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="37ac5-241">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="37ac5-242">**Счет поставщика:** *104*</span><span class="sxs-lookup"><span data-stu-id="37ac5-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="37ac5-243">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="37ac5-244">Выберите **ОК** и запишите номер заказа.</span><span class="sxs-lookup"><span data-stu-id="37ac5-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="37ac5-245">Новая строка добавляется на экспресс-вкладку **Строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="37ac5-246">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-247">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="37ac5-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="37ac5-248">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="37ac5-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="37ac5-249">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="37ac5-249">Create a sales order</span></span>

<span data-ttu-id="37ac5-250">Выполните следующие действия, чтобы создать заказ на продажу в качестве источника спроса.</span><span class="sxs-lookup"><span data-stu-id="37ac5-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="37ac5-251">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="37ac5-252">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="37ac5-253">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="37ac5-254">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="37ac5-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="37ac5-255">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="37ac5-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="37ac5-256">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-256">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-257">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="37ac5-258">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37ac5-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="37ac5-259">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="37ac5-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="37ac5-260">**Количество:** *3*</span><span class="sxs-lookup"><span data-stu-id="37ac5-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="37ac5-261">Создание планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="37ac5-261">Create planned cross-docking</span></span>

<span data-ttu-id="37ac5-262">Выполните следующие действия, чтобы создать плановый кросс-докинг из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="37ac5-263">На странице **Сведения о заказе на продажу** для только что созданного заказа на продажу на панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Выпуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="37ac5-264">Действие выпуска на склад создает строку отгрузки и строку загрузки для строки заказа на продажу и пытается распределить запасы.</span><span class="sxs-lookup"><span data-stu-id="37ac5-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="37ac5-265">Вы получаете информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="37ac5-265">You receive an informational message.</span></span> <span data-ttu-id="37ac5-266">Вы также получите следующее предупреждение: "Не было создано работ для волны XXXX.</span><span class="sxs-lookup"><span data-stu-id="37ac5-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="37ac5-267">Дополнительные сведения см. в журнале создания работ".</span><span class="sxs-lookup"><span data-stu-id="37ac5-267">See the work creation history log for details."</span></span> <span data-ttu-id="37ac5-268">Это ожидаемое поведение, поскольку склад не содержит запасов.</span><span class="sxs-lookup"><span data-stu-id="37ac5-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="37ac5-269">На экспресс-вкладке **Строки заказа на продажу** в меню **Склад** над сеткой выберите **Сведения об отгрузке**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="37ac5-270">Отображается страница **Сведения об отгрузке**, на которой отображается отгрузка, которая была создана для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="37ac5-271">На экспресс-вкладке **Строки загрузки** обратите внимание, что в поле **Количество планового кросс-докинга** установлено значение *3*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="37ac5-272">Так как на складе нет доступных запасов, но допустимый источник поставки прибудет в окне времени, определенном в шаблоне кросс-докинга, было создано количество кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="37ac5-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="37ac5-273">На экспресс-вкладке **Строки загрузки** выберите **Плановый кросс-докинг**, чтобы просмотреть сведения о созданном кросс-докинге.</span><span class="sxs-lookup"><span data-stu-id="37ac5-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="37ac5-274">Обработка кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="37ac5-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="37ac5-275">Получение заказа на покупку в мобильном приложении склада</span><span class="sxs-lookup"><span data-stu-id="37ac5-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="37ac5-276">Система получит количество 5 из заказа на покупку в местонахождение приемки и создаст два этапа работы.</span><span class="sxs-lookup"><span data-stu-id="37ac5-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="37ac5-277">Создаваемый код первой работы имеет для параметра **Тип заказа на работу** значение *Кросс-докинг* и связан с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="37ac5-278">Он имеет количество 3 и направлен в конечное местонахождение отгрузки, чтобы его можно было немедленно отгрузить.</span><span class="sxs-lookup"><span data-stu-id="37ac5-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="37ac5-279">Создаваемый код второй работы имеет для параметра **Тип заказа на работу** значение *Заказы на покупку* и связан с заказом на покупку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="37ac5-280">Она имеет оставшееся количество, равное 2, которое не было переброшено кросс-докингом, и направлена из размещения на хранении.</span><span class="sxs-lookup"><span data-stu-id="37ac5-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="37ac5-281">Выполните вход на мобильном устройстве как пользователь на складе *51*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="37ac5-282">Перейти к пункту **Входящие \> Получение покупки**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="37ac5-283">В поле **PONum** введите свой номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="37ac5-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="37ac5-284">В поле **Кол-во** введите *5*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="37ac5-285">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-285">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-286">На следующей странице задайте для поля **Номенклатура** значение *A0001*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="37ac5-287">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-287">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-288">На следующей странице подтвердите значения **PONum**, **Номенклатура** и **Кол-во**, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="37ac5-289">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="37ac5-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="37ac5-290">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="37ac5-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="37ac5-291">Размещение в кросс-докинге и сборном местонахождении</span><span class="sxs-lookup"><span data-stu-id="37ac5-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="37ac5-292">В настоящее время оба кода работы имеют одинаковое целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="37ac5-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="37ac5-293">Для выполнения следующих шагов необходимо получить код работы чего и код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="37ac5-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="37ac5-294">Эту информацию можно получить на основе сведений о работе для строки заказа на покупку и строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="37ac5-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="37ac5-295">Кроме того, можно перейти к пункту **Управление складом \> Работа \> Сведения о работе** и отфильтровать работу, где значение **Склад** равно *51*.</span><span class="sxs-lookup"><span data-stu-id="37ac5-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="37ac5-296">На мобильном устройстве перейдите к пункту **Входящие \> Размещение покупок** и введите целевое грузоместо из работы.</span><span class="sxs-lookup"><span data-stu-id="37ac5-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="37ac5-297">В поле **Код** введите код целевого грузоместа из сведений о работе.</span><span class="sxs-lookup"><span data-stu-id="37ac5-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="37ac5-298">На странице комплектации кросс-докинга отображается местонахождение комплектации (*RECV*), целевое грузоместо (*грузоместо*), номенклатура (*A0001*) и количество (*3*).</span><span class="sxs-lookup"><span data-stu-id="37ac5-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="37ac5-299">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-299">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-300">В поле **Целевое грузоместо** введите целевое грузоместо для кода грузоместа, который должен быть помещен (с использованием кросс-докинга) в местонахождение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="37ac5-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="37ac5-301">Можно выбрать любой код грузоместа по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="37ac5-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="37ac5-302">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-302">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-303">На следующей странице в поле **Код** введите код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="37ac5-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="37ac5-304">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-304">Select **OK**.</span></span>
1. <span data-ttu-id="37ac5-305">Подтвердите работу по комплектации оставшегося количества, равного 2, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="37ac5-306">На следующей странице выберите **Готово**, чтобы завершить процесс комплектации и начать процесс размещения.</span><span class="sxs-lookup"><span data-stu-id="37ac5-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="37ac5-307">Мобильное приложение показывает вам местонахождение и грузоместо для размещения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="37ac5-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="37ac5-308">Подтвердите операцию **Поместить** в сборное местонахождение, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="37ac5-309">На следующей странице подтвердите операцию **Поместить** с помощью кросс-докинг, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="37ac5-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="37ac5-310">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="37ac5-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="37ac5-311">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="37ac5-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="37ac5-312">На следующем рисунке показано, как может выглядеть завершенная работа кросс-докинга в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="37ac5-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="37ac5-313">![Завершенная работа кросс-докинга](media/PlannedCrossDockingWork.png "Завершенная работа кросс-докинга")</span><span class="sxs-lookup"><span data-stu-id="37ac5-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]