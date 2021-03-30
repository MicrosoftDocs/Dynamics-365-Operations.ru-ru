---
title: Позиционирование грузоместа в местонахождении
description: Позиционирование местонахождения грузоместа позволяет увидеть, где находится грузоместо в местонахождении с несколькими палетами, например, в местонахождении со стойками глубиной в две палеты.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cfab8c36adb08f799305a153589926bfc1ae31fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217109"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="fd0bd-103">Позиционирование грузоместа в местонахождении</span><span class="sxs-lookup"><span data-stu-id="fd0bd-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd0bd-104">Позиционирование местонахождения грузоместа позволяет увидеть, где находится грузоместо в местонахождении с несколькими палетами, например, в местонахождении со стойками глубиной в две палеты.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="fd0bd-105">Функция добавляет порядковый номер для каждого грузоместа, которое помещается в место хранения.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="fd0bd-106">Этот порядковый номер используется для упорядочения грузомест в местонахождении хранения.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="fd0bd-107">Таким образом, функция интеллектуально поддерживает сценарии, в которых клиенты используют гравитационную систему стоек и должны знать, для целей комплектации, какое грузоместо обращено наружу.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="fd0bd-108">В этом разделе представлен сценарий, который показывает, как настроить и использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="fd0bd-109">Включите функцию позиционирования местонахождения грузомест</span><span class="sxs-lookup"><span data-stu-id="fd0bd-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="fd0bd-110">Прежде чем использовать функцию позиционирования местонахождения грузоместа, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="fd0bd-111">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="fd0bd-112">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fd0bd-113">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fd0bd-114">**Имя функции:** *позиционирование местонахождения грузомест*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fd0bd-115">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="fd0bd-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="fd0bd-116">Сделать образцы данных доступными</span><span class="sxs-lookup"><span data-stu-id="fd0bd-116">Make sample data available</span></span>

<span data-ttu-id="fd0bd-117">Для работы с этим сценарием с помощью предложенных здесь значений следует работать с системой, в которой установлены образцы данных.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="fd0bd-118">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="fd0bd-119">Настройка функции для этого сценария</span><span class="sxs-lookup"><span data-stu-id="fd0bd-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="fd0bd-120">Выполните следующие процедуры, чтобы настроить функцию *Позиционирование местонахождения грузомест* для сценария, представленного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="fd0bd-121">Профили местонахождения</span><span class="sxs-lookup"><span data-stu-id="fd0bd-121">Location profiles</span></span>

<span data-ttu-id="fd0bd-122">Эта функция должна быть включена в профиле местоположения для каждого местоположения, где она будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="fd0bd-123">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="fd0bd-124">В списке профилей местоположения в левой области выберите **НАВГРУЗ-06**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="fd0bd-125">На экспресс-вкладке **Общая** этой функцией были добавлены два новых параметра.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="fd0bd-126">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-126">Set the following values:</span></span>

    - <span data-ttu-id="fd0bd-127">**Включить позицию грузоместа:** *Да*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="fd0bd-128">Если этот параметр имеет значение *Да*, позиция грузоместа будет поддерживаться для грузомест в местоположении.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="fd0bd-129">**Показать позицию грузоместа в мобильном устройстве:** *Да*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="fd0bd-130">Если этот параметр имеет значение *Да*, позиция грузоместа будет отображаться для пользователей мобильных устройств во время корректировки и инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="fd0bd-131">Значение этого параметра можно изменить только тогда, когда функция включена.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="fd0bd-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="fd0bd-133">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="fd0bd-133">Location directives</span></span>

1. <span data-ttu-id="fd0bd-134">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="fd0bd-135">В левой области убедитесь, что в поле **Тип заказа на работу** установлено значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="fd0bd-136">В списке директив местоположения выберите **61 Заказ на комплектацию заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="fd0bd-137">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fd0bd-138">На экспресс-вкладке **Строки** выберите строку со значением **Порядковый номер**, равным *2*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="fd0bd-139">На экспресс-вкладке **Действия для директивы местоположения** выберите строку, имеющую значение **Имя**, равное *Комплектовать для менее чем палета* (это должна быть единственная строка), и измените значение **Порядковый номер** на *2*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="fd0bd-140">Выберите **Создать** над сеткой, чтобы добавить строку для нового действия директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="fd0bd-141">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fd0bd-142">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="fd0bd-143">**Имя:** *Комплектовать позицию 1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="fd0bd-144">Пока новая строка остается выбранной, выберите **Изменить запрос** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="fd0bd-145">В редакторе запросов выберите вкладку **Объединения**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="fd0bd-146">Разверните объединение таблицы **Местоположения**, чтобы отобразить присоединение к таблице **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="fd0bd-147">Разверните объединение таблицы **Складские аналитики**, чтобы отобразить присоединение к таблице **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="fd0bd-148">Выберите **Складские аналитики**, затем выберите **Добавить присоединение к таблице**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="fd0bd-149">В списке таблиц, которые отображаются, в столбце **Отношение** выберите **Грузоместо (грузоместо)**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="fd0bd-150">Затем выберите **Выбрать**, чтобы добавить **Грузоместо** в объединение таблицы **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="fd0bd-151">Пока все еще выбрано **Грузоместо**, выберите **Добавить соединение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="fd0bd-152">В списке таблиц, которые отображаются, в столбце **Отношение** выберите **Позиционирование местонахождения грузомест (грузоместо)**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="fd0bd-153">Затем выберите **Выбрать**, чтобы добавить **Позиционирование местонахождения грузомест** в объединение таблицы **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="fd0bd-154">![Соединения таблиц](media/LpTableJoin.png "Соединения таблиц")</span><span class="sxs-lookup"><span data-stu-id="fd0bd-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="fd0bd-155">Выберите **ОК**, чтобы подтвердить обновленные соединяемые таблицы, и закройте редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="fd0bd-156">На экспресс-вкладке **Действия директивы местоположения** снова выберите **Изменить запрос**, чтобы снова открыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="fd0bd-157">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="fd0bd-158">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fd0bd-159">**Таблица:** *Позиционирование местонахождения грузомест*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="fd0bd-160">**Производная таблица:** *Позиционирование местонахождения грузомест*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="fd0bd-161">**Поле:** *Позиция грузоместа*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="fd0bd-162">**Критерий:** *1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="fd0bd-163">![Новый диапазон](media/LpPositionCriteria.png "Новый диапазон")</span><span class="sxs-lookup"><span data-stu-id="fd0bd-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="fd0bd-164">Выберите **ОК**, чтобы подтвердить изменения и закрыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="fd0bd-165">Настройка образца данных для этого сценария</span><span class="sxs-lookup"><span data-stu-id="fd0bd-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="fd0bd-166">Для этого сценария пользователь должен выполнить вход в мобильное приложение склада, используя сотрудника, настроенного для работы на складе *61*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="fd0bd-167">Кроме того, пользователь должен выполнить проводки.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-167">The user must also complete transactions.</span></span>

<span data-ttu-id="fd0bd-168">Поскольку функция *Позиционирование позиции грузоместа* добавляет новый идентификатор для позиций грузоместа в местоположении, необходимо сначала создать для поддержки этого сценария какие-либо данные.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="fd0bd-169">Подсчет наличия в первом местоположении</span><span class="sxs-lookup"><span data-stu-id="fd0bd-169">Spot-count the first location</span></span>

1. <span data-ttu-id="fd0bd-170">Откройте мобильное приложение склада и войдите на склад *61*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="fd0bd-171">Перейдите к пункту **Запасы \> Подсчет наличия**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="fd0bd-172">На странице **Подсчет наличия** задайте в поле **Местоположение** значение *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="fd0bd-173">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-173">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-174">На странице отображается введенное местоположение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-174">The page shows the location that you entered.</span></span> <span data-ttu-id="fd0bd-175">На ней также показано следующее сообщение: "Местонахождение завершено, добавить новое грузоместо или номенклатуру?"</span><span class="sxs-lookup"><span data-stu-id="fd0bd-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="fd0bd-176">Выберите **Обновить** для добавления подсчета в местонахождение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="fd0bd-177">В поле **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Номенклатура**, затем введите значение *A0001*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="fd0bd-178">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-178">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-179">На странице **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Грузоместо**, затем введите значение *LP1001* (или любой другой номер грузоместа по вашему выбору).</span><span class="sxs-lookup"><span data-stu-id="fd0bd-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="fd0bd-180">Страница **Цикличный подсчет: добавление нового грузоместа или номенклатуры** отображается **Позиция грузоместа 1**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="fd0bd-181">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-181">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-182">Теперь необходимо указать количество номенклатуры, которое подсчитано на грузоместе.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="fd0bd-183">Задайте в поле **Кол-во** значение *10*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="fd0bd-184">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-184">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-185">На странице отображается введенное местоположение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-185">The page shows the location that you entered.</span></span> <span data-ttu-id="fd0bd-186">На ней также показано следующее сообщение: "Местонахождение завершено, добавить новое грузоместо или номенклатуру?"</span><span class="sxs-lookup"><span data-stu-id="fd0bd-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="fd0bd-187">Выберите **Обновить** для добавления другого подсчета в местонахождение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="fd0bd-188">В поле **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Номенклатура**, затем введите значение *A0002*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="fd0bd-189">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-189">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-190">На странице **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Грузоместо**, затем введите значение *LP1002* (или любой другой номер грузоместа по вашему выбору, если он отличается от номера грузоместа, указанного ранее).</span><span class="sxs-lookup"><span data-stu-id="fd0bd-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="fd0bd-191">Измените позицию грузоместа, установив для поля **Позиция грузоместа** значение *2*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="fd0bd-192">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-192">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-193">Укажите количество номенклатуры, которое подсчитывается на грузоместе, задав для поля **Кол-во** значение *10*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="fd0bd-194">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-194">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-195">На странице отображается введенное местоположение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-195">The page shows the location that you entered.</span></span> <span data-ttu-id="fd0bd-196">На ней также показано следующее сообщение: "Местонахождение завершено, добавить новое грузоместо или номенклатуру?"</span><span class="sxs-lookup"><span data-stu-id="fd0bd-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="fd0bd-197">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-197">Select **OK**.</span></span>

<span data-ttu-id="fd0bd-198">Работа теперь завершена.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="fd0bd-199">Подсчет наличия во втором местоположении</span><span class="sxs-lookup"><span data-stu-id="fd0bd-199">Spot-count the second location</span></span>

1. <span data-ttu-id="fd0bd-200">На странице **Подсчет наличия** задайте в поле **Местоположение** значение *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="fd0bd-201">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-201">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-202">На странице отображается введенное местоположение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-202">The page shows the location that you entered.</span></span> <span data-ttu-id="fd0bd-203">На ней также показано следующее сообщение: "Местонахождение завершено, добавить новое грузоместо или номенклатуру?"</span><span class="sxs-lookup"><span data-stu-id="fd0bd-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="fd0bd-204">Выберите **Обновить** для добавления подсчета в местонахождение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="fd0bd-205">В поле **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Номенклатура**, затем введите значение *A0002*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="fd0bd-206">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-206">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-207">На странице **Цикличный подсчет: добавление нового грузоместа или номенклатуры** выберите поле **Грузоместо**, затем введите значение *LP1003* (или любой другой номер грузоместа по вашему выбору, если он отличается от обоих номеров грузомест, указанных в предыдущей процедуре).</span><span class="sxs-lookup"><span data-stu-id="fd0bd-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="fd0bd-208">Страница **Цикличный подсчет: добавление нового грузоместа или номенклатуры** отображается **Позиция грузоместа 1**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="fd0bd-209">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-209">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-210">Укажите количество номенклатуры, которое подсчитывается на грузоместе, задав для поля **Кол-во** значение *10*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="fd0bd-211">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-211">Select **OK**.</span></span>

    <span data-ttu-id="fd0bd-212">На странице отображается введенное местоположение.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-212">The page shows the location that you entered.</span></span> <span data-ttu-id="fd0bd-213">На ней также показано следующее сообщение: "Местонахождение завершено, добавить новое грузоместо или номенклатуру?"</span><span class="sxs-lookup"><span data-stu-id="fd0bd-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="fd0bd-214">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-214">Select **OK**.</span></span>

<span data-ttu-id="fd0bd-215">Работа теперь завершена.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="fd0bd-216">Сведения о работе</span><span class="sxs-lookup"><span data-stu-id="fd0bd-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="fd0bd-217">Подсчеты наличия из работы создания подсчета циклов из мобильного приложения в Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="fd0bd-218">Для работы требуется, чтобы подсчеты были приняты перед разноской в запасы.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="fd0bd-219">Войдите в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="fd0bd-220">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="fd0bd-221">На вкладке **Обзор** найдите строки, имеющие следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="fd0bd-222">**Тип заказа на работу:** *Циклический подсчет*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="fd0bd-223">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="fd0bd-224">**Состояние работы:** *Ожидание проверки*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="fd0bd-225">Для этих строк должны быть созданы два кода рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="fd0bd-226">Должны быть приняты подсчеты для обоих этих кодов работ.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="fd0bd-227">В сетке выберите код первой работы для типа заказа на работу *Циклический подсчет*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="fd0bd-228">в области действий на вкладке **Работа** в группе **Работа** выберите **Циклический подсчет**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="fd0bd-229">Отображаются две строки, по одной для каждой номенклатуры и грузоместа.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="fd0bd-230">Значения в полях **Подсчитанное количество**, **Местонахождение**, **Грузоместо** и **Номенклатура** должны совпадать с записями инвентаризации, созданными на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="fd0bd-231">Если какое-либо из этих полей не отображается, выберите **Отобразить аналитики** на панели операций, чтобы добавить их в сетку.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="fd0bd-232">Выберите обе строки.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-232">Select both lines.</span></span>
1. <span data-ttu-id="fd0bd-233">На панели операций выберите **Принять подсчет**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="fd0bd-234">Вы получаете сообщение "Разноска — журнал".</span><span class="sxs-lookup"><span data-stu-id="fd0bd-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="fd0bd-235">Выберите **Сведения о сообщении** для просмотра номера разнесенного журнала.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="fd0bd-236">Закройте сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-236">Close the message details.</span></span>
1. <span data-ttu-id="fd0bd-237">Обновите страницу **Работа**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="fd0bd-238">Первый код работы был закрыт и больше не отображается.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="fd0bd-239">Чтобы просмотреть закрытую работу, установите флажок **Показать закрытые** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="fd0bd-240">Теперь вы примите работу для грузоместа в местонахождении *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="fd0bd-241">На вкладке **Обзор** выберите код второй работы для типа заказа на работу *Циклический подсчет*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="fd0bd-242">в области действий на вкладке **Работа** в группе **Работа** выберите **Циклический подсчет**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="fd0bd-243">Отображается одна строка, для номенклатуры и грузоместа.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="fd0bd-244">Значения в полях **Подсчитанное количество**, **Местонахождение**, **Грузоместо** и **Номенклатура** должны совпадать с записями инвентаризации, созданными на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="fd0bd-245">Выберите строку.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-245">Select the line.</span></span>
1. <span data-ttu-id="fd0bd-246">На панели операций выберите **Принять подсчет**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="fd0bd-247">Вы получаете сообщение "Разноска — журнал".</span><span class="sxs-lookup"><span data-stu-id="fd0bd-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="fd0bd-248">Выберите **Сведения о сообщении** для просмотра номера разнесенного журнала.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="fd0bd-249">Закройте сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-249">Close the message details.</span></span>
1. <span data-ttu-id="fd0bd-250">Обновите страницу **Работа**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="fd0bd-251">Второй код работы был закрыт и больше не отображается.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="fd0bd-252">Чтобы просмотреть закрытую работу, установите флажок **Показать закрытые** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="fd0bd-253">В наличии по местонахождению</span><span class="sxs-lookup"><span data-stu-id="fd0bd-253">On-hand by location</span></span>

1. <span data-ttu-id="fd0bd-254">Перейдите в раздел **Управление складом \> Запросы и отчеты \> В наличии по местонахождению**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="fd0bd-255">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-255">Set the following values:</span></span>

    - <span data-ttu-id="fd0bd-256">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-256">**Site:** *6*</span></span>
    - <span data-ttu-id="fd0bd-257">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="fd0bd-258">**Обновить по местоположениям:** *Да*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="fd0bd-259">Обратите внимание на то, что местоположение *01A01R1S1B* имеет два грузоместа:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="fd0bd-260">**A0001**, где для поля **Позиция грузоместа** указано значение *1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="fd0bd-261">**A0002**, где для поля **Позиция грузоместа** указано значение *2*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="fd0bd-262">Обратите внимание на то, что местоположение *01A01R1S2B* имеет одно грузоместо:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="fd0bd-263">**A0002**, где для поля **Позиция грузоместа** указано значение *1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="fd0bd-264">Сценарий заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="fd0bd-264">Sales order scenario</span></span>

<span data-ttu-id="fd0bd-265">Теперь, когда функция *Позиционирование местонахождения грузомест* настроена, и запасы были помещены на временное хранение, необходимо создать заказ на продажу для создания работы по комплектации, которая будет направлять работника склада для комплектации номенклатуры *A0002* из местоположения запасов, в котором указан код палеты в позиции *1*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="fd0bd-266">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="fd0bd-267">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="fd0bd-268">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fd0bd-269">**Счет клиента:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="fd0bd-270">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="fd0bd-271">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-271">Select **OK**.</span></span>
1. <span data-ttu-id="fd0bd-272">Новая строка добавляется в сетку на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="fd0bd-273">В этой новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd0bd-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="fd0bd-274">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="fd0bd-275">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="fd0bd-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="fd0bd-276">В меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="fd0bd-277">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов для строки заказа.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="fd0bd-278">Закройте страницу **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="fd0bd-279">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="fd0bd-280">Вы получаете информационное сообщение, которое указывают код волны и код отгрузки, которые были созданы для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="fd0bd-281">На экспресс-вкладке **Строки заказа на продажу** в меню **Склад** над сеткой выберите **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="fd0bd-282">Отображается страница **Работа**, на которой отображается работа, которая была создана для данной строки продажи.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="fd0bd-283">Запишите отображаемый код работы.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="fd0bd-284">Сценарий комплектации продаж</span><span class="sxs-lookup"><span data-stu-id="fd0bd-284">Sales picking scenario</span></span>

1. <span data-ttu-id="fd0bd-285">Откройте мобильное приложение и войдите на склад *61*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="fd0bd-286">Выберите **Исходящие \> Комплектация продаж**.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="fd0bd-287">На странице **Сканирование кода работы / кода грузоместа** выберите поле **Код**, затем введите код работы из строки продаж.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="fd0bd-288">Обратите внимание, что работа комплектации направляет вас для комплектации номенклатуры *A0002* из местонахождения *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="fd0bd-289">Эта инструкция выводится в связи с тем, что номенклатура *A0002* находится на грузоместе, расположенном в позиции *1* в этом местоположении.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="fd0bd-290">![Местонахождение позиции 1](media/LocationLicensePlatePositioning.png "Местонахождение позиции 1")</span><span class="sxs-lookup"><span data-stu-id="fd0bd-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="fd0bd-291">Введите код грузоместа, который был создан для местоположения, затем следуйте инструкциям для комплектации заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]