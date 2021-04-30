---
title: Плановый кросс-докинг
description: В этой теме описывается усовершенствованный плановый кросс-докинг, где количество запасов, необходимое для заказа, направляется прямо из приемки или создания в правильный дебаркадер отгрузки или промежуточную область. Все остальные запасы из входящего источника направляются в правильное место хранения через процесс обычного размещения.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911256"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="b2499-104">Плановый кросс-докинг</span><span class="sxs-lookup"><span data-stu-id="b2499-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2499-105">В этой теме описывается расширенный плановый кросс-докинг.</span><span class="sxs-lookup"><span data-stu-id="b2499-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="b2499-106">Кросс-докинг — это складской процесс, где количество запасов, необходимое для заказа, направляется прямо из приемки или создания в правильный дебаркадер отгрузки или промежуточную область.</span><span class="sxs-lookup"><span data-stu-id="b2499-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="b2499-107">Все остальные запасы из входящего источника направляются в правильное место хранения через процесс обычного размещения.</span><span class="sxs-lookup"><span data-stu-id="b2499-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="b2499-108">Кросс-докинг позволяет сотрудникам пропускать входящее размещение и исходящую комплектацию запасов, уже помеченных для исходящего заказа.</span><span class="sxs-lookup"><span data-stu-id="b2499-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="b2499-109">Таким образом, число случаев, когда запасы затрагиваются, уменьшается, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="b2499-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="b2499-110">Кроме того, поскольку имеется меньше взаимодействия с системой, увеличивается экономия времени и места складирования на складе.</span><span class="sxs-lookup"><span data-stu-id="b2499-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="b2499-111">Прежде чем можно будет выполнить кросс-докинг, вам нужно настроить новый шаблон кросс-докинга, где указаны источник поставок и другие наборы требований для кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="b2499-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="b2499-112">При создании исходящего заказа строка должна быть помечена для входящего заказа, который содержит ту же номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b2499-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="b2499-113">Можно выбрать поле код директивы в шаблоне кросс-докинга подобно способу настройки заказов на пополнение запасов и заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="b2499-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="b2499-114">Во время получения входящего заказа настройка кросс-докинга автоматически определяет потребность в кросс-докинге и создает работу перемещения для требуемого количества на основе настройки директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="b2499-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="b2499-115">При отмене работы кросс-докинга регистрация складских проводок *не* отменяется, даже если настройка для этой возможности включена в параметрах управления складом.</span><span class="sxs-lookup"><span data-stu-id="b2499-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="b2499-116">Включение функций планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="b2499-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="b2499-117">Если ваша система еще не содержит функций, описанных в этом разделе, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="b2499-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="b2499-118">*Плановый кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="b2499-119">*Шаблоны кросс-докинга с директивами мест хранения*</span><span class="sxs-lookup"><span data-stu-id="b2499-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="b2499-120">Эта функция позволяет указать поле **код директивы** в шаблоне кросс-докинга, как и способ настройки шаблонов пополнения.</span><span class="sxs-lookup"><span data-stu-id="b2499-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="b2499-121">Включение этой функции предотвращает добавление кода директивы в строки рабочего шаблона кросс-докинга для окончательной строки *Put*.</span><span class="sxs-lookup"><span data-stu-id="b2499-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="b2499-122">Это гарантирует, что место окончательного размещения можно определить во время создания работы перед рассмотрением рабочих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="b2499-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="b2499-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="b2499-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="b2499-124">Повторное создание методов разноски загрузки</span><span class="sxs-lookup"><span data-stu-id="b2499-124">Regenerate load posting methods</span></span>

<span data-ttu-id="b2499-125">Плановый кросс-докинг реализован как метод разноски загрузки.</span><span class="sxs-lookup"><span data-stu-id="b2499-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="b2499-126">После включения функции необходимо повторно создать методы.</span><span class="sxs-lookup"><span data-stu-id="b2499-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="b2499-127">Перейдите в раздел **Управление складом \> Настройка \> Методы разноски загрузки**.</span><span class="sxs-lookup"><span data-stu-id="b2499-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="b2499-128">В области операций выберите **Восстановить методы**.</span><span class="sxs-lookup"><span data-stu-id="b2499-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="b2499-129">После завершения повторного создания должен отобразиться метод со значение **Имя метода**, равным *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="b2499-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="b2499-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2499-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="b2499-131">Создание шаблона кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="b2499-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="b2499-132">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны кросс-докинга**.</span><span class="sxs-lookup"><span data-stu-id="b2499-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="b2499-133">На панели операций выберите **Создать** для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="b2499-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="b2499-134">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="b2499-135">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="b2499-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="b2499-136">Это поле определяет порядок, в котором оцениваются шаблоны.</span><span class="sxs-lookup"><span data-stu-id="b2499-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="b2499-137">**Код шаблона кросс-докинга:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="b2499-138">**Описание:** *Склад 51*</span><span class="sxs-lookup"><span data-stu-id="b2499-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="b2499-139">**Политика выпуска спроса:** *Перед получением поставки*</span><span class="sxs-lookup"><span data-stu-id="b2499-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="b2499-140">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b2499-141">Настройка на экспресс-вкладке **Планирование** управляет тем, как будет работать шаблон.</span><span class="sxs-lookup"><span data-stu-id="b2499-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="b2499-142">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-142">Set the following values:</span></span>

    - <span data-ttu-id="b2499-143">**Требования к спросу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b2499-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="b2499-144">Это поле определяет требования к запасам спроса.</span><span class="sxs-lookup"><span data-stu-id="b2499-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="b2499-145">Если спрос должен быть связан с поставками до выпуска, выберите *Маркировка*.</span><span class="sxs-lookup"><span data-stu-id="b2499-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="b2499-146">Если спрос должен быть зарезервирован по заказам для поставок до выпуска, выберите *Резервирование заказа*.</span><span class="sxs-lookup"><span data-stu-id="b2499-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="b2499-147">**Тип местонахождения:** *Местонахождения отгрузок*</span><span class="sxs-lookup"><span data-stu-id="b2499-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="b2499-148">Это поле определяет, должна ли работа кросс-докинга использовать местоположения промежуточного хранения/загрузки из отгрузки, или следует ли использовать директивы местоположения для поиска собственных местоположений промежуточного хранения/загрузки.</span><span class="sxs-lookup"><span data-stu-id="b2499-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="b2499-149">**Шаблон работы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="b2499-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="b2499-150">Это поле определяет шаблон работы, который должен использоваться при создании работы по кросс-докингу.</span><span class="sxs-lookup"><span data-stu-id="b2499-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="b2499-151">**Повторная проверка при поступлении поставок:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b2499-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="b2499-152">Этот параметр определяет, должна ли поставка быть повторно проверена в ходе приемки.</span><span class="sxs-lookup"><span data-stu-id="b2499-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="b2499-153">Если этот параметр имеет значение *Да*, проверяются как максимальный промежуток времени, так и диапазон дней истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="b2499-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="b2499-154">**Код директивы:** оставьте это поле пустым</span><span class="sxs-lookup"><span data-stu-id="b2499-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="b2499-155">Этот параметр доступен для функции *Шаблоны кросс-докинга с директивами мест хранения*.</span><span class="sxs-lookup"><span data-stu-id="b2499-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="b2499-156">Система использует директивы местоположения, чтобы определить оптимальное местоположение для перемещения в него запасов кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="b2499-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="b2499-157">Настройку можно выполнить, назначив код директивы каждому соответствующему шаблону кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="b2499-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="b2499-158">Если этот код директивы задан, когда создается работа, система будет искать директивы местонахождения по коду директивы.</span><span class="sxs-lookup"><span data-stu-id="b2499-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="b2499-159">Таким образом можно ограничить директивы местонахождения, используемые для конкретного шаблона кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="b2499-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="b2499-160">**Проверка окна времени:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b2499-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="b2499-161">Этот параметр определяет, следует ли оценивать максимальное окно времени при выборе источника поставки.</span><span class="sxs-lookup"><span data-stu-id="b2499-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="b2499-162">Если для этого параметра установлено значение *Да*, становятся доступны поля, которые относятся к максимальному и минимальному окну времени.</span><span class="sxs-lookup"><span data-stu-id="b2499-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="b2499-163">**Максимальное временное окно:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2499-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="b2499-164">Это поле определяет максимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="b2499-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b2499-165">**Единица максимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="b2499-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b2499-166">**Минимальное временное окно:** *0*</span><span class="sxs-lookup"><span data-stu-id="b2499-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="b2499-167">Это поле определяет минимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="b2499-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b2499-168">**Единица минимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="b2499-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b2499-169">**Диапазон истечения срока действия в днях:** *0*</span><span class="sxs-lookup"><span data-stu-id="b2499-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="b2499-170">*Критерий первоочередного отпуска товаров с ближайшим сроком годности (FEFO):* в этом поле определяется максимальное число дней между ближайшей датой окончания срока годности партии, которая в настоящее время находится на складе, и полученной партией.</span><span class="sxs-lookup"><span data-stu-id="b2499-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="b2499-171">На экспресс-вкладке **Источники поставок** указываются типы поставок, которые действительны для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="b2499-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="b2499-172">Выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b2499-173">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="b2499-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b2499-174">**Источник поставок:** *Заказ на покупку*</span><span class="sxs-lookup"><span data-stu-id="b2499-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="b2499-175">Создание класса работ</span><span class="sxs-lookup"><span data-stu-id="b2499-175">Create a work class</span></span>

1. <span data-ttu-id="b2499-176">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="b2499-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b2499-177">На панели операций выберите **Создать** для создания класса работ.</span><span class="sxs-lookup"><span data-stu-id="b2499-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="b2499-178">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-178">Set the following values:</span></span>

    - <span data-ttu-id="b2499-179">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b2499-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b2499-180">**Описание:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="b2499-181">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="b2499-182">Создание шаблона работы</span><span class="sxs-lookup"><span data-stu-id="b2499-182">Create a work template</span></span>

1. <span data-ttu-id="b2499-183">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="b2499-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b2499-184">Задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="b2499-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b2499-185">На панели операций выберите **Создать**, чтобы добавить строку на вкладку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="b2499-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="b2499-186">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2499-187">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="b2499-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b2499-188">**Шаблон работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="b2499-189">**Описание шаблона работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="b2499-190">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Сведения о шаблоне работы**.</span><span class="sxs-lookup"><span data-stu-id="b2499-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b2499-191">На экспресс-вкладке **Сведения о шаблоне работы** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b2499-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2499-192">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2499-193">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="b2499-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b2499-194">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b2499-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b2499-195">Выберите **Создать**, чтобы добавить еще одну строку, и установите следующие значения в ней:</span><span class="sxs-lookup"><span data-stu-id="b2499-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="b2499-196">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="b2499-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b2499-197">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b2499-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b2499-198">Выберите **Сохранить** и убедитесь, что установлен флажок **Допустимый** для шаблона *51 Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="b2499-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="b2499-199">Коды классов работ для типов работ *Комплектация* и *Размещение* должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="b2499-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="b2499-200">Создание директив местонахождения</span><span class="sxs-lookup"><span data-stu-id="b2499-200">Create location directives</span></span>

1. <span data-ttu-id="b2499-201">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="b2499-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b2499-202">В левой панели задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="b2499-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b2499-203">На панели действий выберите **Создать**, затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="b2499-204">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="b2499-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b2499-205">**Имя:** *51 кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="b2499-206">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="b2499-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b2499-207">**Сайт:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2499-207">**Site:** *5*</span></span>
    - <span data-ttu-id="b2499-208">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b2499-209">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="b2499-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b2499-210">На экспресс-вкладке **Строки** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b2499-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2499-211">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2499-212">**Количество "От":** *1*</span><span class="sxs-lookup"><span data-stu-id="b2499-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b2499-213">**Количество "До":** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b2499-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="b2499-214">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="b2499-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b2499-215">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b2499-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2499-216">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2499-217">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="b2499-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="b2499-218">**Использование фиксированного местоположения:** *Фиксированные и нефиксированные местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b2499-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="b2499-219">Выберите **Сохранить**, чтобы сделать доступной кнопку **Изменить запрос** на панели инструментов **Действия директив местоположения**.</span><span class="sxs-lookup"><span data-stu-id="b2499-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="b2499-220">Выберите **Изменить запрос**, чтобы открыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="b2499-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="b2499-221">На вкладке **Диапазон** убедитесь, что настроены следующие две строки:</span><span class="sxs-lookup"><span data-stu-id="b2499-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="b2499-222">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="b2499-222">Line 1:</span></span>

        - <span data-ttu-id="b2499-223">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b2499-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b2499-224">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b2499-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b2499-225">**Поле:** *Склад*</span><span class="sxs-lookup"><span data-stu-id="b2499-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="b2499-226">**Критерий:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="b2499-227">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="b2499-227">Line 2:</span></span>

        - <span data-ttu-id="b2499-228">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b2499-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b2499-229">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b2499-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b2499-230">**Поле:** *Местонахождение*</span><span class="sxs-lookup"><span data-stu-id="b2499-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="b2499-231">**Критерий:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="b2499-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="b2499-232">Выберите **ОК**, чтобы закрыть редактор запроса.</span><span class="sxs-lookup"><span data-stu-id="b2499-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b2499-233">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b2499-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b2499-234">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b2499-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b2499-235">В списке пунктов меню в левой области выберите вариант **Размещение покупки**.</span><span class="sxs-lookup"><span data-stu-id="b2499-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="b2499-236">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b2499-236">Select **Edit**.</span></span>
1. <span data-ttu-id="b2499-237">На экспресс-вкладке **Классы работ** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b2499-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2499-238">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2499-239">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b2499-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b2499-240">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="b2499-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="b2499-241">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b2499-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b2499-242">Сценарий</span><span class="sxs-lookup"><span data-stu-id="b2499-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b2499-243">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="b2499-243">Create a purchase order</span></span>

<span data-ttu-id="b2499-244">Выполните следующие действия, чтобы создать заказ на покупку в качестве источника поставки.</span><span class="sxs-lookup"><span data-stu-id="b2499-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="b2499-245">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b2499-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b2499-246">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b2499-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2499-247">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2499-248">**Счет поставщика:** *104*</span><span class="sxs-lookup"><span data-stu-id="b2499-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b2499-249">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b2499-250">Выберите **ОК** и запишите номер заказа.</span><span class="sxs-lookup"><span data-stu-id="b2499-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="b2499-251">Новая строка добавляется на экспресс-вкладку **Строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b2499-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b2499-252">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2499-253">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b2499-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b2499-254">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2499-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b2499-255">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="b2499-255">Create a sales order</span></span>

<span data-ttu-id="b2499-256">Выполните следующие действия, чтобы создать заказ на продажу в качестве источника спроса.</span><span class="sxs-lookup"><span data-stu-id="b2499-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="b2499-257">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b2499-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b2499-258">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b2499-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2499-259">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2499-260">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b2499-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b2499-261">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="b2499-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b2499-262">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-262">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-263">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b2499-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2499-264">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b2499-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2499-265">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b2499-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b2499-266">**Количество:** *3*</span><span class="sxs-lookup"><span data-stu-id="b2499-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="b2499-267">Создание планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="b2499-267">Create planned cross-docking</span></span>

<span data-ttu-id="b2499-268">Выполните следующие действия, чтобы создать плановый кросс-докинг из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b2499-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="b2499-269">На странице **Сведения о заказе на продажу** для только что созданного заказа на продажу на панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Выпуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="b2499-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b2499-270">Действие выпуска на склад создает строку отгрузки и строку загрузки для строки заказа на продажу и пытается распределить запасы.</span><span class="sxs-lookup"><span data-stu-id="b2499-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="b2499-271">Вы получаете информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="b2499-271">You receive an informational message.</span></span> <span data-ttu-id="b2499-272">Вы также получите следующее предупреждение: "Не было создано работ для волны XXXX.</span><span class="sxs-lookup"><span data-stu-id="b2499-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="b2499-273">Дополнительные сведения см. в журнале создания работ".</span><span class="sxs-lookup"><span data-stu-id="b2499-273">See the work creation history log for details."</span></span> <span data-ttu-id="b2499-274">Это ожидаемое поведение, поскольку склад не содержит запасов.</span><span class="sxs-lookup"><span data-stu-id="b2499-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="b2499-275">На экспресс-вкладке **Строки заказа на продажу** в меню **Склад** над сеткой выберите **Сведения об отгрузке**.</span><span class="sxs-lookup"><span data-stu-id="b2499-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="b2499-276">Отображается страница **Сведения об отгрузке**, на которой отображается отгрузка, которая была создана для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b2499-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="b2499-277">На экспресс-вкладке **Строки загрузки** обратите внимание, что в поле **Количество планового кросс-докинга** установлено значение *3*.</span><span class="sxs-lookup"><span data-stu-id="b2499-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="b2499-278">Так как на складе нет доступных запасов, но допустимый источник поставки прибудет в окне времени, определенном в шаблоне кросс-докинга, было создано количество кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="b2499-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="b2499-279">На экспресс-вкладке **Строки загрузки** выберите **Плановый кросс-докинг**, чтобы просмотреть сведения о созданном кросс-докинге.</span><span class="sxs-lookup"><span data-stu-id="b2499-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="b2499-280">Обработка кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="b2499-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="b2499-281">Получение заказа на покупку в мобильном приложении склада</span><span class="sxs-lookup"><span data-stu-id="b2499-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="b2499-282">Система получит количество 5 из заказа на покупку в местонахождение приемки и создаст два этапа работы.</span><span class="sxs-lookup"><span data-stu-id="b2499-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="b2499-283">Создаваемый код первой работы имеет для параметра **Тип заказа на работу** значение *Кросс-докинг* и связан с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="b2499-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="b2499-284">Он имеет количество 3 и направлен в конечное местонахождение отгрузки, чтобы его можно было немедленно отгрузить.</span><span class="sxs-lookup"><span data-stu-id="b2499-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="b2499-285">Создаваемый код второй работы имеет для параметра **Тип заказа на работу** значение *Заказы на покупку* и связан с заказом на покупку.</span><span class="sxs-lookup"><span data-stu-id="b2499-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="b2499-286">Она имеет оставшееся количество, равное 2, которое не было переброшено кросс-докингом, и направлена из размещения на хранении.</span><span class="sxs-lookup"><span data-stu-id="b2499-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="b2499-287">Выполните вход на мобильном устройстве как пользователь на складе *51*.</span><span class="sxs-lookup"><span data-stu-id="b2499-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b2499-288">Перейти к пункту **Входящие \> Получение покупки**.</span><span class="sxs-lookup"><span data-stu-id="b2499-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="b2499-289">В поле **PONum** введите свой номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="b2499-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="b2499-290">В поле **Кол-во** введите *5*.</span><span class="sxs-lookup"><span data-stu-id="b2499-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="b2499-291">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-291">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-292">На следующей странице задайте для поля **Номенклатура** значение *A0001*.</span><span class="sxs-lookup"><span data-stu-id="b2499-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="b2499-293">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-293">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-294">На следующей странице подтвердите значения **PONum**, **Номенклатура** и **Кол-во**, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="b2499-295">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="b2499-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b2499-296">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="b2499-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="b2499-297">Размещение в кросс-докинге и сборном местонахождении</span><span class="sxs-lookup"><span data-stu-id="b2499-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="b2499-298">В настоящее время оба кода работы имеют одинаковое целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="b2499-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="b2499-299">Для выполнения следующих шагов необходимо получить код работы чего и код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="b2499-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="b2499-300">Эту информацию можно получить на основе сведений о работе для строки заказа на покупку и строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="b2499-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="b2499-301">Кроме того, можно перейти к пункту **Управление складом \> Работа \> Сведения о работе** и отфильтровать работу, где значение **Склад** равно *51*.</span><span class="sxs-lookup"><span data-stu-id="b2499-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="b2499-302">На мобильном устройстве перейдите к пункту **Входящие \> Размещение покупок** и введите целевое грузоместо из работы.</span><span class="sxs-lookup"><span data-stu-id="b2499-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="b2499-303">В поле **Код** введите код целевого грузоместа из сведений о работе.</span><span class="sxs-lookup"><span data-stu-id="b2499-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="b2499-304">На странице комплектации кросс-докинга отображается местонахождение комплектации (*RECV*), целевое грузоместо (*грузоместо*), номенклатура (*A0001*) и количество (*3*).</span><span class="sxs-lookup"><span data-stu-id="b2499-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="b2499-305">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-305">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-306">В поле **Целевое грузоместо** введите целевое грузоместо для кода грузоместа, который должен быть помещен (с использованием кросс-докинга) в местонахождение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="b2499-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="b2499-307">Можно выбрать любой код грузоместа по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="b2499-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="b2499-308">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-308">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-309">На следующей странице в поле **Код** введите код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="b2499-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="b2499-310">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-310">Select **OK**.</span></span>
1. <span data-ttu-id="b2499-311">Подтвердите работу по комплектации оставшегося количества, равного 2, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="b2499-312">На следующей странице выберите **Готово**, чтобы завершить процесс комплектации и начать процесс размещения.</span><span class="sxs-lookup"><span data-stu-id="b2499-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="b2499-313">Мобильное приложение показывает вам местонахождение и грузоместо для размещения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b2499-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="b2499-314">Подтвердите операцию **Поместить** в сборное местонахождение, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="b2499-315">На следующей странице подтвердите операцию **Поместить** с помощью кросс-докинг, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b2499-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="b2499-316">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="b2499-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b2499-317">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="b2499-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="b2499-318">На следующем рисунке показано, как может выглядеть завершенная работа кросс-докинга в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b2499-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b2499-319">![Завершенная работа кросс-докинга](media/PlannedCrossDockingWork.png "Завершенная работа кросс-докинга")</span><span class="sxs-lookup"><span data-stu-id="b2499-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]