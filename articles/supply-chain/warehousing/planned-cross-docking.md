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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017767"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d86c5-104">Плановый кросс-докинг</span><span class="sxs-lookup"><span data-stu-id="d86c5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d86c5-105">В этой теме описывается расширенный плановый кросс-докинг.</span><span class="sxs-lookup"><span data-stu-id="d86c5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d86c5-106">Кросс-докинг — это складской процесс, где количество запасов, необходимое для заказа, направляется прямо из приемки или создания в правильный дебаркадер отгрузки или промежуточную область.</span><span class="sxs-lookup"><span data-stu-id="d86c5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d86c5-107">Все остальные запасы из входящего источника направляются в правильное место хранения через процесс обычного размещения.</span><span class="sxs-lookup"><span data-stu-id="d86c5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d86c5-108">Кросс-докинг позволяет сотрудникам пропускать входящее размещение и исходящую комплектацию запасов, уже помеченных для исходящего заказа.</span><span class="sxs-lookup"><span data-stu-id="d86c5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d86c5-109">Таким образом, число случаев, когда запасы затрагиваются, уменьшается, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="d86c5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d86c5-110">Кроме того, поскольку имеется меньше взаимодействия с системой, увеличивается экономия времени и места складирования на складе.</span><span class="sxs-lookup"><span data-stu-id="d86c5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d86c5-111">Прежде чем можно будет выполнить кросс-докинг, пользователь должен настроить новый шаблон кросс-докинга, где указаны источник поставок и другие наборы требований для кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="d86c5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d86c5-112">При создании исходящего заказа строка должна быть помечена для входящего заказа, который содержит ту же номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="d86c5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="d86c5-113">Во время получения входящего заказа настройка кросс-докинга автоматически определяет потребность в кросс-докинге и создает работу перемещения для требуемого количества на основе настройки директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="d86c5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d86c5-114">При отмене работы кросс-докинга регистрация складских проводок **не** отменяется, даже если настройка для этой возможности включена в параметрах управления складом.</span><span class="sxs-lookup"><span data-stu-id="d86c5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="d86c5-115">Включение функции планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="d86c5-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="d86c5-116">Прежде чем можно будет использовать расширенный плановый кросс-докинг, в системе должна быть включена эта функция.</span><span class="sxs-lookup"><span data-stu-id="d86c5-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="d86c5-117">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="d86c5-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d86c5-118">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d86c5-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d86c5-119">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="d86c5-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d86c5-120">**Название функции:** *Плановый кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="d86c5-121">Настройка</span><span class="sxs-lookup"><span data-stu-id="d86c5-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d86c5-122">Повторное создание методов разноски загрузки</span><span class="sxs-lookup"><span data-stu-id="d86c5-122">Regenerate load posting methods</span></span>

<span data-ttu-id="d86c5-123">Плановый кросс-докинг реализован как метод разноски загрузки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d86c5-124">После включения функции необходимо повторно создать методы.</span><span class="sxs-lookup"><span data-stu-id="d86c5-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d86c5-125">Перейдите в раздел **Управление складом \> Настройка \> Методы разноски загрузки**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d86c5-126">В области операций выберите **Восстановить методы**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d86c5-127">После завершения повторного создания должен отобразиться метод со значение **Имя метода** , равным *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d86c5-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d86c5-129">Создание шаблона кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="d86c5-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="d86c5-130">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны кросс-докинга**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d86c5-131">На панели операций выберите **Создать** для создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="d86c5-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d86c5-132">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="d86c5-133">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="d86c5-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="d86c5-134">Это поле определяет порядок, в котором оцениваются шаблоны.</span><span class="sxs-lookup"><span data-stu-id="d86c5-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d86c5-135">**Код шаблона кросс-докинга:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d86c5-136">**Описание:** *Склад 51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d86c5-137">**Политика выпуска спроса:** *Перед получением поставки*</span><span class="sxs-lookup"><span data-stu-id="d86c5-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d86c5-138">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d86c5-139">Настройка на экспресс-вкладке **Планирование** управляет тем, как будет работать шаблон.</span><span class="sxs-lookup"><span data-stu-id="d86c5-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d86c5-140">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-140">Set the following values:</span></span>

    - <span data-ttu-id="d86c5-141">**Требования к спросу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="d86c5-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d86c5-142">Это поле определяет требования к запасам спроса.</span><span class="sxs-lookup"><span data-stu-id="d86c5-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d86c5-143">Если спрос должен быть связан с поставками до выпуска, выберите *Маркировка*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d86c5-144">Если спрос должен быть зарезервирован по заказам для поставок до выпуска, выберите *Резервирование заказа*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d86c5-145">**Тип местонахождения:** *Местонахождения отгрузок*</span><span class="sxs-lookup"><span data-stu-id="d86c5-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d86c5-146">Это поле определяет, должна ли работа кросс-докинга использовать местоположения промежуточного хранения/загрузки из отгрузки, или следует ли использовать директивы местоположения для поиска собственных местоположений промежуточного хранения/загрузки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d86c5-147">**Шаблон работы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="d86c5-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d86c5-148">Это поле определяет шаблон работы, который должен использоваться при создании работы по кросс-докингу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d86c5-149">**Повторная проверка при поступлении поставок:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="d86c5-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d86c5-150">Этот параметр определяет, должна ли поставка быть повторно проверена в ходе приемки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d86c5-151">Если этот параметр имеет значение *Да* , проверяются как максимальный промежуток времени, так и диапазон дней истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="d86c5-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d86c5-152">**Проверка окна времени:** *Да*</span><span class="sxs-lookup"><span data-stu-id="d86c5-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d86c5-153">Этот параметр определяет, следует ли оценивать максимальное окно времени при выборе источника поставки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d86c5-154">Если для этого параметра установлено значение *Да* , становятся доступны поля, которые относятся к максимальному и минимальному окну времени.</span><span class="sxs-lookup"><span data-stu-id="d86c5-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d86c5-155">**Максимальное временное окно:** *5*</span><span class="sxs-lookup"><span data-stu-id="d86c5-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d86c5-156">Это поле определяет максимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d86c5-157">**Единица максимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="d86c5-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d86c5-158">**Минимальное временное окно:** *0*</span><span class="sxs-lookup"><span data-stu-id="d86c5-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d86c5-159">Это поле определяет минимальный допустимый временной период между поступлением поставки и убытием по спросу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d86c5-160">**Единица минимального окна времени:** *Дни*</span><span class="sxs-lookup"><span data-stu-id="d86c5-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d86c5-161">**Диапазон истечения срока действия в днях:** *0*</span><span class="sxs-lookup"><span data-stu-id="d86c5-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d86c5-162">*Критерий первоочередного отпуска товаров с ближайшим сроком годности (FEFO):* в этом поле определяется максимальное число дней между ближайшей датой окончания срока годности партии, которая в настоящее время находится на складе, и полученной партией.</span><span class="sxs-lookup"><span data-stu-id="d86c5-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d86c5-163">На экспресс-вкладке **Источники поставок** указываются типы поставок, которые действительны для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="d86c5-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d86c5-164">Выберите **Создать** , затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="d86c5-165">**Порядковый номер** : *1*</span><span class="sxs-lookup"><span data-stu-id="d86c5-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d86c5-166">**Источник поставок:** *Заказ на покупку*</span><span class="sxs-lookup"><span data-stu-id="d86c5-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d86c5-167">Создание класса работ</span><span class="sxs-lookup"><span data-stu-id="d86c5-167">Create a work class</span></span>

1. <span data-ttu-id="d86c5-168">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d86c5-169">На панели операций выберите **Создать** для создания класса работ.</span><span class="sxs-lookup"><span data-stu-id="d86c5-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d86c5-170">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-170">Set the following values:</span></span>

    - <span data-ttu-id="d86c5-171">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d86c5-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d86c5-172">**Описание:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d86c5-173">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d86c5-174">Создание шаблона работы</span><span class="sxs-lookup"><span data-stu-id="d86c5-174">Create a work template</span></span>

1. <span data-ttu-id="d86c5-175">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d86c5-176">Задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d86c5-177">На панели операций выберите **Создать** , чтобы добавить строку на вкладку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d86c5-178">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-179">**Порядковый номер** : *1*</span><span class="sxs-lookup"><span data-stu-id="d86c5-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d86c5-180">**Шаблон работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d86c5-181">**Описание шаблона работы:** *51 Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d86c5-182">Выберите **Сохранить** , чтобы сделать доступной экспресс-вкладку **Сведения о шаблоне работы**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d86c5-183">На экспресс-вкладке **Сведения о шаблоне работы** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d86c5-184">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-185">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="d86c5-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d86c5-186">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d86c5-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d86c5-187">Выберите **Создать** , чтобы добавить еще одну строку, и установите следующие значения в ней:</span><span class="sxs-lookup"><span data-stu-id="d86c5-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d86c5-188">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="d86c5-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d86c5-189">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d86c5-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d86c5-190">Выберите **Сохранить** и убедитесь, что установлен флажок **Допустимый** для шаблона *51 Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d86c5-191">Коды классов работ для типов работ *Комплектация* и *Размещение* должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="d86c5-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d86c5-192">Создание директив местонахождения</span><span class="sxs-lookup"><span data-stu-id="d86c5-192">Create location directives</span></span>

1. <span data-ttu-id="d86c5-193">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d86c5-194">В левой панели задайте в поле **Тип заказа на работу** значение *Кросс-докинг*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d86c5-195">На панели действий выберите **Создать** , затем задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="d86c5-196">**Порядковый номер** : *1*</span><span class="sxs-lookup"><span data-stu-id="d86c5-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d86c5-197">**Имя:** *51 кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d86c5-198">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="d86c5-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d86c5-199">**Сайт:** *5*</span><span class="sxs-lookup"><span data-stu-id="d86c5-199">**Site:** *5*</span></span>
    - <span data-ttu-id="d86c5-200">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d86c5-201">Выберите **Сохранить** , чтобы сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d86c5-202">На экспресс-вкладке **Строки** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d86c5-203">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-204">**Количество "От":** *1*</span><span class="sxs-lookup"><span data-stu-id="d86c5-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d86c5-205">**Количество "До":** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d86c5-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d86c5-206">Выберите **Сохранить** , чтобы сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d86c5-207">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d86c5-208">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-209">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="d86c5-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d86c5-210">**Использование фиксированного местоположения:** *Фиксированные и нефиксированные местонахождения*</span><span class="sxs-lookup"><span data-stu-id="d86c5-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d86c5-211">Выберите **Сохранить** , чтобы сделать доступной кнопку **Изменить запрос** на панели инструментов **Действия директив местоположения**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d86c5-212">Выберите **Изменить запрос** , чтобы открыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="d86c5-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d86c5-213">На вкладке **Диапазон** убедитесь, что настроены следующие две строки:</span><span class="sxs-lookup"><span data-stu-id="d86c5-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d86c5-214">Строка 1:</span><span class="sxs-lookup"><span data-stu-id="d86c5-214">Line 1:</span></span>

        - <span data-ttu-id="d86c5-215">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="d86c5-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d86c5-216">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="d86c5-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d86c5-217">**Поле:** *Склад*</span><span class="sxs-lookup"><span data-stu-id="d86c5-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d86c5-218">**Критерий:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d86c5-219">Строка 2:</span><span class="sxs-lookup"><span data-stu-id="d86c5-219">Line 2:</span></span>

        - <span data-ttu-id="d86c5-220">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="d86c5-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d86c5-221">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="d86c5-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d86c5-222">**Поле:** *Местонахождение*</span><span class="sxs-lookup"><span data-stu-id="d86c5-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="d86c5-223">**Критерий:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="d86c5-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d86c5-224">Выберите **ОК** , чтобы закрыть редактор запроса.</span><span class="sxs-lookup"><span data-stu-id="d86c5-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d86c5-225">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="d86c5-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d86c5-226">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d86c5-227">В списке пунктов меню в левой области выберите вариант **Размещение покупки**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d86c5-228">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-228">Select **Edit**.</span></span>
1. <span data-ttu-id="d86c5-229">На экспресс-вкладке **Классы работ** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d86c5-230">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-231">**Код класса работы:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d86c5-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d86c5-232">**Тип заказа на работу:** *Кросс-докинг*</span><span class="sxs-lookup"><span data-stu-id="d86c5-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d86c5-233">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d86c5-234">Сценарий</span><span class="sxs-lookup"><span data-stu-id="d86c5-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d86c5-235">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="d86c5-235">Create a purchase order</span></span>

<span data-ttu-id="d86c5-236">Выполните следующие действия, чтобы создать заказ на покупку в качестве источника поставки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d86c5-237">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d86c5-238">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d86c5-239">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d86c5-240">**Счет поставщика:** *104*</span><span class="sxs-lookup"><span data-stu-id="d86c5-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d86c5-241">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d86c5-242">Выберите **ОК** и запишите номер заказа.</span><span class="sxs-lookup"><span data-stu-id="d86c5-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="d86c5-243">Новая строка добавляется на экспресс-вкладку **Строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d86c5-244">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-245">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d86c5-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d86c5-246">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="d86c5-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d86c5-247">Создать заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="d86c5-247">Create a sales order</span></span>

<span data-ttu-id="d86c5-248">Выполните следующие действия, чтобы создать заказ на продажу в качестве источника спроса.</span><span class="sxs-lookup"><span data-stu-id="d86c5-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d86c5-249">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d86c5-250">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d86c5-251">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d86c5-252">**Счет клиента:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d86c5-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d86c5-253">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="d86c5-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d86c5-254">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-254">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-255">Новая строка добавляется на экспресс-вкладку **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d86c5-256">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d86c5-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="d86c5-257">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d86c5-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d86c5-258">**Количество:** *3*</span><span class="sxs-lookup"><span data-stu-id="d86c5-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d86c5-259">Создание планового кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="d86c5-259">Create planned cross-docking</span></span>

<span data-ttu-id="d86c5-260">Выполните следующие действия, чтобы создать плановый кросс-докинг из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d86c5-261">На странице **Сведения о заказе на продажу** для только что созданного заказа на продажу на панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Выпуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d86c5-262">Действие выпуска на склад создает строку отгрузки и строку загрузки для строки заказа на продажу и пытается распределить запасы.</span><span class="sxs-lookup"><span data-stu-id="d86c5-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d86c5-263">Вы получаете информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d86c5-263">You receive an informational message.</span></span> <span data-ttu-id="d86c5-264">Вы также получите следующее предупреждение: "Не было создано работ для волны XXXX.</span><span class="sxs-lookup"><span data-stu-id="d86c5-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d86c5-265">Дополнительные сведения см. в журнале создания работ".</span><span class="sxs-lookup"><span data-stu-id="d86c5-265">See the work creation history log for details."</span></span> <span data-ttu-id="d86c5-266">Это ожидаемое поведение, поскольку склад не содержит запасов.</span><span class="sxs-lookup"><span data-stu-id="d86c5-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d86c5-267">На экспресс-вкладке **Строки заказа на продажу** в меню **Склад** над сеткой выберите **Сведения об отгрузке**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d86c5-268">Отображается страница **Сведения об отгрузке** , на которой отображается отгрузка, которая была создана для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d86c5-269">На экспресс-вкладке **Строки загрузки** обратите внимание, что в поле **Количество планового кросс-докинга** установлено значение *3*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d86c5-270">Так как на складе нет доступных запасов, но допустимый источник поставки прибудет в окне времени, определенном в шаблоне кросс-докинга, было создано количество кросс-докинга.</span><span class="sxs-lookup"><span data-stu-id="d86c5-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d86c5-271">На экспресс-вкладке **Строки загрузки** выберите **Плановый кросс-докинг** , чтобы просмотреть сведения о созданном кросс-докинге.</span><span class="sxs-lookup"><span data-stu-id="d86c5-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d86c5-272">Обработка кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="d86c5-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d86c5-273">Получение заказа на покупку в мобильном приложении склада</span><span class="sxs-lookup"><span data-stu-id="d86c5-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d86c5-274">Система получит количество 5 из заказа на покупку в местонахождение приемки и создаст два этапа работы.</span><span class="sxs-lookup"><span data-stu-id="d86c5-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d86c5-275">Создаваемый код первой работы имеет для параметра **Тип заказа на работу** значение *Кросс-докинг* и связан с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d86c5-276">Он имеет количество 3 и направлен в конечное местонахождение отгрузки, чтобы его можно было немедленно отгрузить.</span><span class="sxs-lookup"><span data-stu-id="d86c5-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d86c5-277">Создаваемый код второй работы имеет для параметра **Тип заказа на работу** значение *Заказы на покупку* и связан с заказом на покупку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d86c5-278">Она имеет оставшееся количество, равное 2, которое не было переброшено кросс-докингом, и направлена из размещения на хранении.</span><span class="sxs-lookup"><span data-stu-id="d86c5-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d86c5-279">Выполните вход на мобильном устройстве как пользователь на складе *51*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d86c5-280">Перейти к пункту **Входящие \> Получение покупки**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d86c5-281">В поле **PONum** введите свой номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="d86c5-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d86c5-282">В поле **Кол-во** введите *5*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d86c5-283">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-283">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-284">На следующей странице задайте для поля **Номенклатура** значение *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d86c5-285">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-285">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-286">На следующей странице подтвердите значения **PONum** , **Номенклатура** и **Кол-во** , выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d86c5-287">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="d86c5-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d86c5-288">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="d86c5-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d86c5-289">Размещение в кросс-докинге и сборном местонахождении</span><span class="sxs-lookup"><span data-stu-id="d86c5-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d86c5-290">В настоящее время оба кода работы имеют одинаковое целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="d86c5-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d86c5-291">Для выполнения следующих шагов необходимо получить код работы чего и код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="d86c5-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d86c5-292">Эту информацию можно получить на основе сведений о работе для строки заказа на покупку и строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="d86c5-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d86c5-293">Кроме того, можно перейти к пункту **Управление складом \> Работа \> Сведения о работе** и отфильтровать работу, где значение **Склад** равно *51*.</span><span class="sxs-lookup"><span data-stu-id="d86c5-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d86c5-294">На мобильном устройстве перейдите к пункту **Входящие \> Размещение покупок** и введите целевое грузоместо из работы.</span><span class="sxs-lookup"><span data-stu-id="d86c5-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d86c5-295">В поле **Код** введите код целевого грузоместа из сведений о работе.</span><span class="sxs-lookup"><span data-stu-id="d86c5-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d86c5-296">На странице комплектации кросс-докинга отображается местонахождение комплектации ( *RECV* ), целевое грузоместо ( *грузоместо* ), номенклатура ( *A0001* ) и количество ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="d86c5-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="d86c5-297">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-297">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-298">В поле **Целевое грузоместо** введите целевое грузоместо для кода грузоместа, который должен быть помещен (с использованием кросс-докинга) в местонахождение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="d86c5-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d86c5-299">Можно выбрать любой код грузоместа по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="d86c5-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d86c5-300">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-300">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-301">На следующей странице в поле **Код** введите код целевого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="d86c5-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d86c5-302">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-302">Select **OK**.</span></span>
1. <span data-ttu-id="d86c5-303">Подтвердите работу по комплектации оставшегося количества, равного 2, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d86c5-304">На следующей странице выберите **Готово** , чтобы завершить процесс комплектации и начать процесс размещения.</span><span class="sxs-lookup"><span data-stu-id="d86c5-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d86c5-305">Мобильное приложение показывает вам местонахождение и грузоместо для размещения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d86c5-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d86c5-306">Подтвердите операцию **Поместить** в сборное местонахождение, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d86c5-307">На следующей странице подтвердите операцию **Поместить** с помощью кросс-докинг, выбрав **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d86c5-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d86c5-308">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="d86c5-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d86c5-309">Выберите **Отмена** для выхода.</span><span class="sxs-lookup"><span data-stu-id="d86c5-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d86c5-310">На следующем рисунке показано, как может выглядеть завершенная работа кросс-докинга в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d86c5-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d86c5-311">![Завершенная работа кросс-докинга](media/PlannedCrossDockingWork.png "Завершенная работа кросс-докинга")</span><span class="sxs-lookup"><span data-stu-id="d86c5-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
