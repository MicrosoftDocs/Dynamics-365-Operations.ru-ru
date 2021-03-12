---
title: Исходящая сортировка
description: В этом разделе представлена информация об исходящей сортировке. Эта функция упрощает обработку небольших контейнеров и помогает сотрудникам склада лучше планировать и организовывать емкость палет в грузовике.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963418"
---
# <a name="outbound-sorting"></a><span data-ttu-id="3fd93-104">Исходящая сортировка</span><span class="sxs-lookup"><span data-stu-id="3fd93-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fd93-105">Эта функция упрощает обработку небольших контейнеров и помогает сотрудникам склада лучше планировать и организовывать емкость палет в грузовике.</span><span class="sxs-lookup"><span data-stu-id="3fd93-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="3fd93-106">При использовании исходящей сортировки упакованные контейнеры можно отсортировать на правильную палету после того, как они были на станции упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="3fd93-107">Также можно создать иерархию упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="3fd93-108">Эта функция позволяет создавать палеты из контейнеров, которые упакованы с помощью функции упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="3fd93-109">Контейнер не отправляется в конечное местонахождение отгрузки, как в исходном потоке упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="3fd93-110">Вместо этого работники могут закрыть контейнер и переместить его в местонахождение типа сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="3fd93-111">Затем они могут сортировать контейнеры для положений, каждое из которых имеет грузоместо (LP).</span><span class="sxs-lookup"><span data-stu-id="3fd93-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="3fd93-112">После сортировки контейнеров можно создать работу для отправки целого грузоместа в конечные местонахождения дока отгрузки или промежуточные местонахождения на основе директив местоположения или ваших собственных требований.</span><span class="sxs-lookup"><span data-stu-id="3fd93-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="3fd93-113">Кроме того, действие по закрытию позиции сортировки может немедленно переместить запасы в конечное местонахождение отгрузки и скомплектовать их в заказ.</span><span class="sxs-lookup"><span data-stu-id="3fd93-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="3fd93-114">Включение функции исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="3fd93-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="3fd93-115">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="3fd93-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="3fd93-116">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="3fd93-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3fd93-117">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3fd93-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3fd93-118">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="3fd93-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3fd93-119">**Название компонента:** *Исходящая сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="3fd93-120">Настройка</span><span class="sxs-lookup"><span data-stu-id="3fd93-120">Setup</span></span>

<span data-ttu-id="3fd93-121">Для этого сценария необходимо использовать стандартные демонстрационные данные **USMF** и склад *62*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="3fd93-122">Кроме того, необходимо выполнить настройку, описанную в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="3fd93-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="3fd93-123">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="3fd93-123">Set up a wave template</span></span>

<span data-ttu-id="3fd93-124">Эта настройка автоматически обрабатывает волну и создает работу при выпуске строки на склад.</span><span class="sxs-lookup"><span data-stu-id="3fd93-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="3fd93-125">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="3fd93-126">В списке шаблонов выберите **Склад 62**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="3fd93-127">На Экспресс-вкладке **Общие** убедитесь, что параметр **Обрабатывать волну перед запуском на склад** имеет значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="3fd93-128">Настройка работника</span><span class="sxs-lookup"><span data-stu-id="3fd93-128">Set up a worker</span></span>

<span data-ttu-id="3fd93-129">Упаковочная станция рассматривается как местонахождение.</span><span class="sxs-lookup"><span data-stu-id="3fd93-129">The packing station is considered a location.</span></span> <span data-ttu-id="3fd93-130">Работники склада, вошедшие на эту упаковочную станцию, видят и работают только с отгрузками и контейнерами, которые планируются в данном местонахождении упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="3fd93-131">Пользователь, вошедший в Microsoft Dynamics 365, должен быть настроен как сотрудник в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="3fd93-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="3fd93-132">Если имя пользователя не отображается в списке рабочих пользователей, добавьте его с помощью следующей процедуры.</span><span class="sxs-lookup"><span data-stu-id="3fd93-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="3fd93-133">В этих шагах предполагается, что пользователь уже существует в системе и был связан как сотрудник или работник в модуле **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="3fd93-134">Перейдите в раздел **Управление складом \> Настройка \> Рабочий**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="3fd93-135">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-135">Select **New**.</span></span>
1. <span data-ttu-id="3fd93-136">В поле **Рабочий** выберите целевого пользователя в списке сотрудников.</span><span class="sxs-lookup"><span data-stu-id="3fd93-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="3fd93-137">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-137">Select **Select**.</span></span>
1. <span data-ttu-id="3fd93-138">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3fd93-139">На экспресс-вкладке **Пользователи** выберите **Создать**, чтобы создать учетную запись мобильного устройства, и установите для нее следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-140">**ИД пользователя:** введите уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3fd93-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="3fd93-141">**Имя пользователя:** введите имя для идентификатора.</span><span class="sxs-lookup"><span data-stu-id="3fd93-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="3fd93-142">**Склад по умолчанию:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-143">**Имя меню:** *Главное*</span><span class="sxs-lookup"><span data-stu-id="3fd93-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="3fd93-144">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3fd93-145">Появится диалоговое окно **Установка пароля**, в котором можно создать простой пароль, который пользователь может использовать для входа в мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="3fd93-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="3fd93-146">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-146">Set the following values:</span></span>

    - <span data-ttu-id="3fd93-147">**Пароль:** введите простой пароль.</span><span class="sxs-lookup"><span data-stu-id="3fd93-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="3fd93-148">**Подтверждение пароля:** введите этот же пароль еще раз.</span><span class="sxs-lookup"><span data-stu-id="3fd93-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="3fd93-149">Выберите **Установить пароль**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-149">Select **Set password**.</span></span>

    <span data-ttu-id="3fd93-150">Уведомление в центре поддержки информирует о том, что был установлен пароль для созданного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3fd93-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="3fd93-151">Создание типа местонахождения</span><span class="sxs-lookup"><span data-stu-id="3fd93-151">Create a location type</span></span>

1. <span data-ttu-id="3fd93-152">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Типы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="3fd93-153">В области действий выберите **Создать**, чтобы создать тип местонахождения, и установите для него следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-154">**Тип местоположения:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="3fd93-155">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="3fd93-156">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="3fd93-157">Настройка параметров управления складом</span><span class="sxs-lookup"><span data-stu-id="3fd93-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="3fd93-158">Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="3fd93-159">На вкладке **Общие** на экспресс-вкладке **Типы местонахождения** задайте в поле **Тип местонахождения сортировки** значение *СОРТИРОВКА*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="3fd93-160">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="3fd93-161">Настройка профиля местонахождения</span><span class="sxs-lookup"><span data-stu-id="3fd93-161">Set up a location profile</span></span>

1. <span data-ttu-id="3fd93-162">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="3fd93-163">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-164">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fd93-165">**Код профиля местонахождения:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="3fd93-166">**Имя:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="3fd93-167">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3fd93-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-168">**Формат местонахождения:** *ASRB* (проход-стеллаж-полка-позиция)</span><span class="sxs-lookup"><span data-stu-id="3fd93-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="3fd93-169">**Тип местоположения:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="3fd93-170">**Использовать отслеживание грузомест:** *Да*</span><span class="sxs-lookup"><span data-stu-id="3fd93-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="3fd93-171">**Разрешить смешанные номенклатуры:** *Да* (если для этого параметра задано значение *Да*, параметр **Разрешить смешанные складские партии** автоматически устанавливается в значение *Да* и не может быть изменен отдельно.)</span><span class="sxs-lookup"><span data-stu-id="3fd93-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="3fd93-172">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="3fd93-173">Настройка местонахождения</span><span class="sxs-lookup"><span data-stu-id="3fd93-173">Set up a location</span></span>

1. <span data-ttu-id="3fd93-174">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="3fd93-175">В заголовке снимите флажок **Создать контрольные разряды для местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="3fd93-176">В области действий выберите **Создать**, чтобы создать местонахождение, и установите для него следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-177">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-178">**Местонахождение:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="3fd93-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="3fd93-179">**Код профиля местонахождения:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="3fd93-180">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="3fd93-181">Настройка шаблона исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="3fd93-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="3fd93-182">Шаблон исходящей сортировки определяет, создается ли работа вне ячейки сортировки, и выполняется ли сортировка вручную или автоматически.</span><span class="sxs-lookup"><span data-stu-id="3fd93-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="3fd93-183">Для этого сценария создается шаблон исходящей сортировки для создания палет после упаковочной станции.</span><span class="sxs-lookup"><span data-stu-id="3fd93-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="3fd93-184">Выберите **Управление складом \> Настройка \> Упаковка \> Шаблон исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="3fd93-185">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-186">В заголовке нового шаблона задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="3fd93-187">**Код шаблона исходящей сортировки:** *АвтоРабота*</span><span class="sxs-lookup"><span data-stu-id="3fd93-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="3fd93-188">**Описание:** *Автоматическое создание работы*</span><span class="sxs-lookup"><span data-stu-id="3fd93-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="3fd93-189">**Тип шаблона исходящей сортировки:** *Контейнер*</span><span class="sxs-lookup"><span data-stu-id="3fd93-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="3fd93-190">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-191">**Местонахождение:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="3fd93-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="3fd93-192">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3fd93-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-193">**Проверка сортировки:** *Скан позиции*</span><span class="sxs-lookup"><span data-stu-id="3fd93-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="3fd93-194">**Создание работы при закрытии позиции:** *Да*</span><span class="sxs-lookup"><span data-stu-id="3fd93-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="3fd93-195">Если для этого параметра задано значение *Да*, при закрытии позиции будет создаваться работа для перемещения запасов в конечное местоположение отгрузки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="3fd93-196">Если для него задано значение *Нет*, запасы будут немедленно скомплектованы в заказ при закрытии позиции.</span><span class="sxs-lookup"><span data-stu-id="3fd93-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="3fd93-197">**Назначение позиции:** *Автоматически*</span><span class="sxs-lookup"><span data-stu-id="3fd93-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="3fd93-198">Если в этом поле задано значение *Вручную*, пользователь должен всегда указывать, в какую позицию запасов должна быть выполнена сортировка.</span><span class="sxs-lookup"><span data-stu-id="3fd93-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="3fd93-199">Если в нем задано значение *Автоматически*, система автоматически направляет запасы в позицию, когда это возможно, на основе перерывов шаблона сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="3fd93-200">Выберите **Сохранить**, чтобы сделать доступной кнопку **Изменить запрос** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="3fd93-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="3fd93-201">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="3fd93-202">В редакторе запросов на вкладке **Сортировка** добавьте строку со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="3fd93-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="3fd93-203">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="3fd93-204">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="3fd93-205">**Поле:** *Услуга перевозчика*</span><span class="sxs-lookup"><span data-stu-id="3fd93-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="3fd93-206">При выбора этого значения может появиться следующее сообщение: "Поле услуги перевозчика не является индексным полем.</span><span class="sxs-lookup"><span data-stu-id="3fd93-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="3fd93-207">Хотите добавить сортировку по нему?"</span><span class="sxs-lookup"><span data-stu-id="3fd93-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="3fd93-208">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-208">Select **Yes**.</span></span>

    - <span data-ttu-id="3fd93-209">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="3fd93-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="3fd93-210">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-210">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-211">Может появиться следующее сообщение: "Группирование будет сброшено, продолжить?"</span><span class="sxs-lookup"><span data-stu-id="3fd93-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="3fd93-212">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-212">Select **Yes**.</span></span>

    <span data-ttu-id="3fd93-213">Становится доступной кнопка **Разбиения шаблона исходящей сортировки** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="3fd93-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="3fd93-214">На панели операций выберите **Разбиения шаблона исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="3fd93-215">В диалоговом окне **Критерии исходящей сортировки** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fd93-216">**Имя таблицы ссылок:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="3fd93-217">**Имя поля ссылки:** *Услуга перевозчика*</span><span class="sxs-lookup"><span data-stu-id="3fd93-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="3fd93-218">**Поле для группировки:** установите этот флажок, чтобы сгруппировать отгрузки по услуге перевозчика.</span><span class="sxs-lookup"><span data-stu-id="3fd93-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="3fd93-219">Выберите **ОК**, чтобы сохранить настройки и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3fd93-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="3fd93-220">Настройка политик упаковки контейнеров</span><span class="sxs-lookup"><span data-stu-id="3fd93-220">Set up container packing policies</span></span>

1. <span data-ttu-id="3fd93-221">Перейдите в раздел **Управление складом \> Настройка \> Контейнеры \> Политики упаковки контейнеров**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="3fd93-222">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-223">В заголовке новой политики задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="3fd93-224">**Политика упаковки контейнеров:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-225">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="3fd93-226">На экспресс-вкладке **Обзор** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3fd93-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-227">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-228">**Местоположение по умолчанию для сортировки:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="3fd93-229">**Единица измерения веса:** *кг*</span><span class="sxs-lookup"><span data-stu-id="3fd93-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="3fd93-230">**Политика закрытия контейнера:** *Автоматический выпуск*</span><span class="sxs-lookup"><span data-stu-id="3fd93-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="3fd93-231">**Политика выпуска контейнера:** *Назначить контейнеру позицию исходящей сортировки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="3fd93-232">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="3fd93-233">Настройка профилей упаковки</span><span class="sxs-lookup"><span data-stu-id="3fd93-233">Set up packing profiles</span></span>

<span data-ttu-id="3fd93-234">Создайте новый профиль упаковки, который будет использоваться вместе с функциональностью сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="3fd93-235">Перейдите в раздел **Управление складом \> Настройка \> Упаковка \> Профили упаковки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="3fd93-236">В области действий выберите **Создать**, чтобы создать строку, и установите для нее следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-237">**Код профиля упаковки:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-238">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-239">**Политика упаковки контейнеров:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-240">**Режим кода контейнера:** *Авто*</span><span class="sxs-lookup"><span data-stu-id="3fd93-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="3fd93-241">**Тип контейнера:** *Ящик-крупный*</span><span class="sxs-lookup"><span data-stu-id="3fd93-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="3fd93-242">**Автоматически создавать контейнер при закрытии контейнера:** снят (= *Нет*)</span><span class="sxs-lookup"><span data-stu-id="3fd93-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="3fd93-243">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="3fd93-244">Настройка классов работ</span><span class="sxs-lookup"><span data-stu-id="3fd93-244">Set up work classes</span></span>

<span data-ttu-id="3fd93-245">Настройка класса работ, который будет использоваться вместе с сортировкой.</span><span class="sxs-lookup"><span data-stu-id="3fd93-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="3fd93-246">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="3fd93-247">В области действий выберите **Создать**, чтобы создать класс работы для сортировки, и установите для него следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-248">**Код класса работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-249">**Описание:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-250">**Тип заказа на работу:** *Комплектация сортированных запасов*</span><span class="sxs-lookup"><span data-stu-id="3fd93-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="3fd93-251">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="3fd93-252">Настройка пунктов меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="3fd93-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="3fd93-253">Настройка нового пункта меню паллеты</span><span class="sxs-lookup"><span data-stu-id="3fd93-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="3fd93-254">Создайте пункт меню мобильного устройства для создания палет при сортировке.</span><span class="sxs-lookup"><span data-stu-id="3fd93-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="3fd93-255">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3fd93-256">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-257">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fd93-258">**Имя пункта меню:** *Сборка палеты*</span><span class="sxs-lookup"><span data-stu-id="3fd93-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="3fd93-259">**Заголовок:** *Сборка палеты*</span><span class="sxs-lookup"><span data-stu-id="3fd93-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="3fd93-260">**Режим:** *Косвенный*</span><span class="sxs-lookup"><span data-stu-id="3fd93-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="3fd93-261">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="3fd93-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="3fd93-262">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3fd93-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-263">**Код действия:** *Исходящая сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="3fd93-264">Когда для этого поля установлено значение *Исходящая сортировка*, отображается поле **Код шаблона исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="3fd93-265">**Использовать руководство по процессу:** *Да*</span><span class="sxs-lookup"><span data-stu-id="3fd93-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="3fd93-266">Если для поля **Код действия** задано значение *Исходящая сортировка*, для этого параметра автоматически устанавливается значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="3fd93-267">**Код шаблона исходящей сортировки:** *АвтоРабота*</span><span class="sxs-lookup"><span data-stu-id="3fd93-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="3fd93-268">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="3fd93-269">Настройка нового пункта меню загрузки</span><span class="sxs-lookup"><span data-stu-id="3fd93-269">Set up a new loading menu item</span></span>

<span data-ttu-id="3fd93-270">Затем создайте пункт меню, который позволит пользователям переместить отсортированные складские номенклатуры в место отгрузки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="3fd93-271">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3fd93-272">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-273">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fd93-274">**Название пункта меню:** *Загрузка из сортировки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="3fd93-275">**Заголовок:** *Загрузка из сортировки*</span><span class="sxs-lookup"><span data-stu-id="3fd93-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="3fd93-276">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="3fd93-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="3fd93-277">**Использовать существующую работу:** *Да*</span><span class="sxs-lookup"><span data-stu-id="3fd93-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="3fd93-278">На экспресс-вкладке **Общие** задайте в поле **Кем управляется** значение *Управляется пользователем*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="3fd93-279">На экспресс-вкладке **Классы работы** выберите **Создать**, затем установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3fd93-280">**Код класса работы:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="3fd93-281">**Тип заказа на работу:** *Комплектация сортированных запасов*</span><span class="sxs-lookup"><span data-stu-id="3fd93-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="3fd93-282">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="3fd93-283">Настройка меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="3fd93-283">Set up the mobile device menu</span></span>

<span data-ttu-id="3fd93-284">Теперь необходимо добавить новые пункты меню в меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd93-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="3fd93-285">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="3fd93-286">Выберите меню **Исходящий**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="3fd93-287">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fd93-288">В столбце **Доступные меню и пункты меню** найдите и выберите **Сборка палеты**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="3fd93-289">Выберите кнопку со стрелкой вправо, чтобы переместить пункт **Сборка палеты** в столбец **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="3fd93-290">Кнопки стрелка вверх и стрелка вниз используются для размещения пункта меню **Сборка палеты** в нужном месте меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd93-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="3fd93-291">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-291">Select **Save**.</span></span>
1. <span data-ttu-id="3fd93-292">Повторите эту процедуру для добавления пункта меню **Загрузка из сортировки** в меню **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="3fd93-293">Настройка директив для места хранения</span><span class="sxs-lookup"><span data-stu-id="3fd93-293">Set up location directives</span></span>

<span data-ttu-id="3fd93-294">*Директивы для мест хранения* — это правила, с помощью которых можно определить места комплектации и размещения для перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="3fd93-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="3fd93-295">Теперь необходимо создать правило для управления работой сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="3fd93-296">Настройка директивы одного SKU</span><span class="sxs-lookup"><span data-stu-id="3fd93-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="3fd93-297">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3fd93-298">В левой области измените значение в поле **Тип заказа на работу** на *Комплектация сортированных запасов*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="3fd93-299">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-300">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fd93-301">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-302">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="3fd93-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="3fd93-303">На экспресс-вкладке **Директивы местоположения** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-304">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="3fd93-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3fd93-305">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3fd93-305">**Site:** *6*</span></span>
    - <span data-ttu-id="3fd93-306">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-307">**Несколько SKU:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="3fd93-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="3fd93-308">Выберите **Сохранить**, чтобы сделать доступной панель инструментов на экспресс-вкладке **Строки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="3fd93-309">На экспресс-вкладке **Строки** выберите **Создать**, затем установите следующие значения для новой строки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="3fd93-310">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fd93-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3fd93-311">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-312">**От:** *0*</span><span class="sxs-lookup"><span data-stu-id="3fd93-312">**From:** *0*</span></span>
    - <span data-ttu-id="3fd93-313">**До:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="3fd93-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="3fd93-314">Выберите **Сохранить**, чтобы сделать доступной панель инструментов на экспресс-вкладке **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="3fd93-315">На экспресс-вкладке **Действия директивы местонахождения** выберите **Создать**, затем установите следующие значения для новой строки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="3fd93-316">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fd93-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3fd93-317">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-318">**Имя:** *Поднимающаяся дверь*</span><span class="sxs-lookup"><span data-stu-id="3fd93-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="3fd93-319">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-319">Select **Save**.</span></span>
1. <span data-ttu-id="3fd93-320">На экспресс-вкладке **Действия директивы местоположения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="3fd93-321">В редакторе запросов на вкладке **Диапазон** найдите строку, в которой поле **Поле** имеет значение *Местонахождение*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="3fd93-322">Задайте в поле **Критерии** для этой строки значение *Дверь отсека*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="3fd93-323">Выберите **ОК**, чтобы сохранить настройки и закрыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="3fd93-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="3fd93-324">Настройка директивы нескольких SKU</span><span class="sxs-lookup"><span data-stu-id="3fd93-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="3fd93-325">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3fd93-326">В левой области измените значение в поле **Тип заказа на работу** на *Комплектация сортированных запасов*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="3fd93-327">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-328">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fd93-329">**Последовательность:** *2*</span><span class="sxs-lookup"><span data-stu-id="3fd93-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="3fd93-330">**Имя:** *Дверь отсека, несколько*</span><span class="sxs-lookup"><span data-stu-id="3fd93-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="3fd93-331">На экспресс-вкладке **Директивы местоположения** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-332">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="3fd93-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3fd93-333">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3fd93-333">**Site:** *6*</span></span>
    - <span data-ttu-id="3fd93-334">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-335">**Несколько SKU:** *Да*</span><span class="sxs-lookup"><span data-stu-id="3fd93-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="3fd93-336">Выберите **Сохранить**, чтобы сделать доступной панель инструментов на экспресс-вкладке **Строки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="3fd93-337">На экспресс-вкладке **Строки** выберите **Создать**, затем установите следующие значения для новой строки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="3fd93-338">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fd93-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3fd93-339">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-340">**От:** *0*</span><span class="sxs-lookup"><span data-stu-id="3fd93-340">**From:** *0*</span></span>
    - <span data-ttu-id="3fd93-341">**До:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="3fd93-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="3fd93-342">Выберите **Сохранить**, чтобы сделать доступной панель инструментов на экспресс-вкладке **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="3fd93-343">На экспресс-вкладке **Действия директивы местонахождения** выберите **Создать**, затем установите следующие значения для новой строки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="3fd93-344">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fd93-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3fd93-345">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-346">**Имя:** *Дверь отсека, несколько*</span><span class="sxs-lookup"><span data-stu-id="3fd93-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="3fd93-347">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-347">Select **Save**.</span></span>
1. <span data-ttu-id="3fd93-348">На экспресс-вкладке **Действия директивы местоположения** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="3fd93-349">В редакторе запросов на вкладке **Диапазон** найдите строку, в которой поле **Поле** имеет значение *Местонахождение*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="3fd93-350">Задайте в поле **Критерии** для этой строки значение *Дверь отсека*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="3fd93-351">Выберите **ОК**, чтобы сохранить настройки и закрыть редактор запросов.</span><span class="sxs-lookup"><span data-stu-id="3fd93-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="3fd93-352">Настройка шаблонов работ</span><span class="sxs-lookup"><span data-stu-id="3fd93-352">Set up work templates</span></span>

1. <span data-ttu-id="3fd93-353">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3fd93-354">Измените значение в поле **Тип заказа на работу** на *Комплектация сортированных запасов*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="3fd93-355">На панели операций выберите **Создать** для создания шаблона работ.</span><span class="sxs-lookup"><span data-stu-id="3fd93-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="3fd93-356">На вкладке **Обзор** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-357">**Последовательность:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3fd93-358">**Шаблон работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="3fd93-359">**Описание шаблона работы:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="3fd93-360">Выберите **Сохранить**, чтобы сделать доступной экспресс-вкладку **Сведения о шаблоне работы**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="3fd93-361">На экспресс-вкладке **Сведения о шаблоне работ** выберите **Создать**, чтобы добавить строку, затем установите для нее следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-362">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="3fd93-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="3fd93-363">**Код класса работы:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="3fd93-364">Снова выберите **Создать**, чтобы добавить вторую строку, затем установите следующие значения для нее:</span><span class="sxs-lookup"><span data-stu-id="3fd93-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="3fd93-365">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="3fd93-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3fd93-366">**Код класса работы:** *СОРТИРОВКА*</span><span class="sxs-lookup"><span data-stu-id="3fd93-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="3fd93-367">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="3fd93-368">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3fd93-368">Scenario</span></span>

<span data-ttu-id="3fd93-369">Этот сценарий имитирует ситуацию, в которой упакованные контейнеры должны автоматически сортироваться в разные позиции (палеты) после упаковочной станции, в зависимости от услуги перевозчика.</span><span class="sxs-lookup"><span data-stu-id="3fd93-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="3fd93-370">После того, как все номенклатуры из загрузки упакованы и отсортированы по адресам, палеты будут перемещены к двери отсека.</span><span class="sxs-lookup"><span data-stu-id="3fd93-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="3fd93-371">Создание заказов на продажу и работы комплектации</span><span class="sxs-lookup"><span data-stu-id="3fd93-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="3fd93-372">Создание заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="3fd93-372">Create sales order 1</span></span>

1. <span data-ttu-id="3fd93-373">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3fd93-374">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-375">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fd93-376">**Счет клиента:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="3fd93-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="3fd93-377">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3fd93-378">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3fd93-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="3fd93-379">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="3fd93-380">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3fd93-381">На Экспресс-вкладке **Доставка** в разделе **Транспортировка** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="3fd93-382">**Перевозчик, осуществляющий доставку:** *Воздушный грузовой*</span><span class="sxs-lookup"><span data-stu-id="3fd93-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="3fd93-383">**Услуга перевозчика:** *Air*</span><span class="sxs-lookup"><span data-stu-id="3fd93-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="3fd93-384">Перейдите к представлению **Строки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="3fd93-385">Если новая пустая строка не добавляется автоматически в сетку на экспресс-вкладке **Строки заказа на продажу**, выберите **Добавить строку**, чтобы добавить ее.</span><span class="sxs-lookup"><span data-stu-id="3fd93-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="3fd93-386">В новой строке заказа установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="3fd93-387">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fd93-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3fd93-388">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="3fd93-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="3fd93-389">Пока новая строка заказа все еще выбрана на экспресс-вкладке **Строки заказа на продажу**, в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3fd93-390">На странице **Резервирование** выберите **Резервирование лота**, чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="3fd93-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3fd93-391">Закройте страницу **Резервирование**, чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3fd93-392">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3fd93-393">Вы получаете информационное сообщение, в котором отображаются отгрузка и волна для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="3fd93-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3fd93-394">Запишите код волны и номера кодов отгрузки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="3fd93-395">Заказ на продажу 2</span><span class="sxs-lookup"><span data-stu-id="3fd93-395">Sales order 2</span></span>

1. <span data-ttu-id="3fd93-396">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3fd93-397">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fd93-398">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fd93-399">**Счет клиента:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="3fd93-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="3fd93-400">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3fd93-401">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3fd93-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="3fd93-402">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-402">The new sales order is opened.</span></span> <span data-ttu-id="3fd93-403">Он должно включать новую пустую строку в сетке на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3fd93-404">В этой строке заказа установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="3fd93-405">**Номенклатура:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fd93-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="3fd93-406">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3fd93-407">На экспресс-вкладке **Сведения по строке** на вкладке **Доставка** установите для поля **Способ доставки** значение *Flowe-СТД*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="3fd93-408">На экспресс-вкладке **Строки заказа на продажу** выберите **Добавить строку**, затем установите следующие значения для второй строки заказа.</span><span class="sxs-lookup"><span data-stu-id="3fd93-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="3fd93-409">**Номенклатура:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3fd93-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="3fd93-410">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="3fd93-411">На экспресс-вкладке **Сведения по строке** на вкладке **Доставка** измените значение поля **Способ доставки** на *Air C-Авиа*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="3fd93-412">На экспресс-вкладке **Строки заказа на продажу** выберите первую строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="3fd93-413">Затем в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3fd93-414">На странице **Резервирование** выберите **Резервирование лота**, чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="3fd93-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3fd93-415">Закройте страницу **Резервирование**, чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3fd93-416">На экспресс-вкладке **Строки заказа на продажу** выберите вторую строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="3fd93-417">Затем в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="3fd93-418">На странице **Резервирование** выберите **Резервирование лота**, чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="3fd93-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="3fd93-419">Закройте страницу **Резервирование**, чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3fd93-420">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="3fd93-421">Вы получаете информационное сообщение, в котором отображаются отгрузка и волна для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="3fd93-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="3fd93-422">Обратите внимание, что были созданы два номера кодов волны и два номера кодов отгрузок, по одному для каждого способа доставки по строкам заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="3fd93-423">Получение кодов работ из сведений о работах</span><span class="sxs-lookup"><span data-stu-id="3fd93-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="3fd93-424">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="3fd93-425">На странице отображаются коды работ, которые были созданы из заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="3fd93-426">Используйте коды волн и коды отгрузки из заказов на продажу, созданных вами, для поиска кода работы для каждой волны и отгрузки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="3fd93-427">Запишите эти коды работ, поскольку они понадобятся в последующих шагах.</span><span class="sxs-lookup"><span data-stu-id="3fd93-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="3fd93-428">Обратите внимание на то, что для второго заказа на продажу было создано два кода работ.</span><span class="sxs-lookup"><span data-stu-id="3fd93-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="3fd93-429">Если различные номенклатуры скомплектованы из разных местоположений, создаются отдельные коды работ.</span><span class="sxs-lookup"><span data-stu-id="3fd93-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="3fd93-430">Комплектация номенклатур для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="3fd93-430">Pick items for the sales orders</span></span>

<span data-ttu-id="3fd93-431">Выполните созданную работу, используя мобильное устройство, чтобы переместить номенклатуры на станцию упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="3fd93-432">На мобильном устройстве выполните вход на склад *62*, используя код пользователя, созданный для этого сценария (или идентификатор пользователя существующего пользователя демонстрационных данных).</span><span class="sxs-lookup"><span data-stu-id="3fd93-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="3fd93-433">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3fd93-434">В меню **Исходящее** выберите **Комплектация продаж**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="3fd93-435">В поле **Код** введите код работы, который был создан для заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="3fd93-436">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-436">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-437">На странице **Заказы на продажу — комплектация** введите целевое грузоместо, созданное для заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="3fd93-438">Обратите внимание на то, что отображаются местонахождение комплектации (*без упаковки-001*), номенклатура (*A0001*) и количество (*2 шт.*).</span><span class="sxs-lookup"><span data-stu-id="3fd93-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="3fd93-439">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-439">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-440">Проверьте информацию на странице **Заказы на продажу — размещение**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="3fd93-441">Поле **Местонахождение** должно указывать, что укомплектованные номенклатуры будут находиться в местоположении *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="3fd93-442">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-442">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-443">На странице **Сканирование кода работы/кода грузоместа** вы получаете сообщение "Работа завершена", которое указывает на то, что код работы из заказа на продажу 1 был завершен.</span><span class="sxs-lookup"><span data-stu-id="3fd93-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="3fd93-444">Теперь нужно будет скомплектовать заказ на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="3fd93-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="3fd93-445">В поле **Код** введите код работы, который был создан для заказа на продажу 2, в котором строка 1 содержит номенклатуру *A0001*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="3fd93-446">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-446">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-447">На странице **Заказы на продажу — комплектация** введите целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="3fd93-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="3fd93-448">Обратите внимание на то, что отображаются местонахождение комплектации (*без упаковки-001*), номенклатура (*A0001*) и количество (*1 шт.*).</span><span class="sxs-lookup"><span data-stu-id="3fd93-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="3fd93-449">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-449">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-450">Проверьте информацию на странице **Заказы на продажу — размещение**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="3fd93-451">Поле **Местонахождение** должно указывать, что укомплектованные номенклатуры будут находиться в местоположении *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="3fd93-452">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-452">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-453">На странице **Сканирование кода работы/кода грузоместа** вы получаете сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="3fd93-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="3fd93-454">Это сообщение означает, что код работы из строки 1 заказа на продажу 2 был завершен.</span><span class="sxs-lookup"><span data-stu-id="3fd93-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="3fd93-455">В поле **Код** введите код работы, который был создан для заказа на продажу 2, в котором строка 2 содержит номенклатуру *A0002*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="3fd93-456">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-456">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-457">На странице **Заказы на продажу — комплектация** введите целевое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="3fd93-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="3fd93-458">Обратите внимание на то, что отображаются местонахождение комплектации (*без упаковки-002*), номенклатура (*A0001*) и количество (*1 шт.*).</span><span class="sxs-lookup"><span data-stu-id="3fd93-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="3fd93-459">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-459">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-460">Проверьте информацию на странице **Заказы на продажу — размещение**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="3fd93-461">Поле **Местонахождение** должно указывать, что укомплектованные номенклатуры будут находиться в местоположении *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="3fd93-462">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-462">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-463">На странице **Сканирование кода работы/кода грузоместа** вы получаете сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="3fd93-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="3fd93-464">Это сообщение означает, что код работы из строки 2 заказа на продажу 2 был завершен.</span><span class="sxs-lookup"><span data-stu-id="3fd93-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="3fd93-465">Упаковка заказов на продажу в контейнеры</span><span class="sxs-lookup"><span data-stu-id="3fd93-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="3fd93-466">Упаковка заказа на продажу 1 в контейнеры</span><span class="sxs-lookup"><span data-stu-id="3fd93-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="3fd93-467">Перейдите в раздел **Управление складом \> Упаковка и контейнеризация \> Упаковка**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="3fd93-468">Открывается диалоговое окно **Выбрать станцию упаковки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="3fd93-469">По умолчанию в поле **Работник** должно быть указано имя сотрудника, который был настроен ранее.</span><span class="sxs-lookup"><span data-stu-id="3fd93-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="3fd93-470">Задайте следующие значения для просмотра и работы с отгрузками и контейнерами, которые планируются в указанном местоположении упаковки:</span><span class="sxs-lookup"><span data-stu-id="3fd93-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="3fd93-471">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="3fd93-471">**Site:** *6*</span></span>
    - <span data-ttu-id="3fd93-472">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="3fd93-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3fd93-473">**Местонахождение:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="3fd93-474">**Код профиля упаковки:** *Сортировка*</span><span class="sxs-lookup"><span data-stu-id="3fd93-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="3fd93-475">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3fd93-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="3fd93-476">На странице **Упаковка** в поле **Грузоместо или отгрузка** введите целевое грузоместо для заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="3fd93-477">Затем выберите клавишу **TAB** или **ВВОД** на клавиатуре, чтобы выйти из поля.</span><span class="sxs-lookup"><span data-stu-id="3fd93-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="3fd93-478">В области действий выберите **Создать контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="3fd93-479">Примите все параметры по умолчанию и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="3fd93-480">Запишите код контейнера.</span><span class="sxs-lookup"><span data-stu-id="3fd93-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="3fd93-481">На экспресс-вкладке **Комплектация номенклатур** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-482">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="3fd93-483">**Идентификатор:** номенклатура *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fd93-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="3fd93-484">В области действий выберите **Закрыть контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="3fd93-485">В диалоговом окне **Закрыть контейнер** выберите вариант **Получить вес системы**, чтобы обновить в системе поле **Вес брутто**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="3fd93-486">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-486">Select **OK**.</span></span> <span data-ttu-id="3fd93-487">Контейнер перемещается в местоположение *СОРТИРОВКА* и готов к сортировке.</span><span class="sxs-lookup"><span data-stu-id="3fd93-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="3fd93-488">Создайте второй контейнер, чтобы добавить вторую номенклатуру из грузоместа для заказа на продажу 1 в новый контейнер.</span><span class="sxs-lookup"><span data-stu-id="3fd93-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="3fd93-489">В области действий выберите **Создать контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="3fd93-490">Примите все параметры по умолчанию и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="3fd93-491">Запишите код контейнера.</span><span class="sxs-lookup"><span data-stu-id="3fd93-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="3fd93-492">На экспресс-вкладке **Комплектация номенклатур** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-493">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="3fd93-494">**Идентификатор:** номенклатура *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fd93-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="3fd93-495">В области действий выберите **Закрыть контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="3fd93-496">В диалоговом окне **Закрыть контейнер** выберите вариант **Получить вес системы**, чтобы обновить в системе поле **Вес брутто**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="3fd93-497">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-497">Select **OK**.</span></span> <span data-ttu-id="3fd93-498">Контейнер перемещается в местоположение *СОРТИРОВКА* и готов к сортировке.</span><span class="sxs-lookup"><span data-stu-id="3fd93-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="3fd93-499">Упаковка заказа на продажу 2 в контейнеры</span><span class="sxs-lookup"><span data-stu-id="3fd93-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="3fd93-500">На странице **Упаковка** в поле **Грузоместо или отгрузка** введите целевое грузоместо для строки 1 заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="3fd93-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="3fd93-501">Затем выберите клавишу **TAB** или **ВВОД** на клавиатуре, чтобы выйти из поля.</span><span class="sxs-lookup"><span data-stu-id="3fd93-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="3fd93-502">В области действий выберите **Создать контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="3fd93-503">Примите все параметры по умолчанию и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="3fd93-504">Запишите код контейнера.</span><span class="sxs-lookup"><span data-stu-id="3fd93-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="3fd93-505">На экспресс-вкладке **Комплектация номенклатур** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-506">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="3fd93-507">**Идентификатор:** номенклатура *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fd93-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="3fd93-508">В области действий выберите **Закрыть контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="3fd93-509">В диалоговом окне **Закрыть контейнер** выберите вариант **Получить вес системы**, чтобы обновить в системе поле **Вес брутто**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="3fd93-510">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-510">Select **OK**.</span></span> <span data-ttu-id="3fd93-511">Контейнер перемещается в местоположение *СОРТИРОВКА* и готов к сортировке.</span><span class="sxs-lookup"><span data-stu-id="3fd93-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="3fd93-512">В поле **Грузоместо или отгрузка** введите целевое грузоместо для строки 2 заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="3fd93-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="3fd93-513">Затем выберите клавишу **TAB** или **ВВОД** на клавиатуре, чтобы выйти из поля.</span><span class="sxs-lookup"><span data-stu-id="3fd93-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="3fd93-514">В области действий выберите **Создать контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="3fd93-515">Примите все параметры по умолчанию и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="3fd93-516">Запишите код контейнера.</span><span class="sxs-lookup"><span data-stu-id="3fd93-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="3fd93-517">На экспресс-вкладке **Комплектация номенклатур** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3fd93-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fd93-518">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fd93-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="3fd93-519">**Поле идентификатора:** номенклатура *A0002*</span><span class="sxs-lookup"><span data-stu-id="3fd93-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="3fd93-520">В области действий выберите **Закрыть контейнер**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="3fd93-521">В диалоговом окне **Закрыть контейнер** выберите вариант **Получить вес системы**, чтобы обновить в системе поле **Вес брутто**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="3fd93-522">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-522">Select **OK**.</span></span> <span data-ttu-id="3fd93-523">Контейнер перемещается в местоположение *СОРТИРОВКА* и готов к сортировке.</span><span class="sxs-lookup"><span data-stu-id="3fd93-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="3fd93-524">Чтобы просмотреть сведения о контейнере, перейдите к пункту **Управление складом \> Упаковка и контейнеризация \> Контейнеры** и выполните поиск кодов контейнеров, созданных во время упаковки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="3fd93-525">Сортировка контейнеров</span><span class="sxs-lookup"><span data-stu-id="3fd93-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fd93-526">При доступе к пункту меню **Сборка палеты** в мобильном приложении для выполнения исходящей сортировки отображается кнопка **Заполнено**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="3fd93-527">*Не используйте кнопку **Заполнено** для сортировки или закрытие позиции.*</span><span class="sxs-lookup"><span data-stu-id="3fd93-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="3fd93-528">Кнопка **Заполнено** предоставляется по умолчанию и не может быть отключена или удалена со страницы.</span><span class="sxs-lookup"><span data-stu-id="3fd93-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="3fd93-529">Она не используется для функции *Исходящая сортировка*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="3fd93-530">Сортировка первого контейнера</span><span class="sxs-lookup"><span data-stu-id="3fd93-530">Sort the first container</span></span>

1. <span data-ttu-id="3fd93-531">На мобильном устройстве выполните вход на склад *62*, используя код пользователя, созданный для этого сценария (или идентификатор пользователя существующего пользователя демонстрационных данных).</span><span class="sxs-lookup"><span data-stu-id="3fd93-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="3fd93-532">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3fd93-533">В меню **Исходящее** выберите **Сборка палет**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="3fd93-534">В поле **Грузоместо/контейнер** введите первый код контейнера, связанный с заказом на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="3fd93-535">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-535">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-536">Потому позиции сортировки в данный момент не существуют, необходимо указать ее.</span><span class="sxs-lookup"><span data-stu-id="3fd93-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="3fd93-537">В поле **Код позиции сортировки** введите *SP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="3fd93-538">Так как в настоящее время нет грузоместа, связанного с позицией сортировки *SP01*, необходимо указать его.</span><span class="sxs-lookup"><span data-stu-id="3fd93-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="3fd93-539">В поле **Грузоместо** введите *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="3fd93-540">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-540">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-541">Поскольку проверка позиции сортировки включена, необходимо ввести код позиции сортировки еще раз.</span><span class="sxs-lookup"><span data-stu-id="3fd93-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="3fd93-542">В поле **Код позиции сортировки** введите *SP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="3fd93-543">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-543">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-544">Вы получите сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="3fd93-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="3fd93-545">Чтобы просмотреть позицию сортировки и грузоместо в ней, перейдите в раздел **Управление складом \> Упаковка и контейнеризация \> Назначение позиций исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="3fd93-546">На странице **Назначение позиций исходящей сортировки** отображаются все позиции сортировки, активные в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3fd93-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="3fd93-547">В поле **Проводки позиций сортировки** отображается грузоместо, связанное с каждой позицией сортировки, и контейнеры, которые находятся в этой позиции сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="3fd93-548">Обратите внимание на то, что в данный момент имеется одна позиция сортировки, а на экспресс-вкладке **Критерий позиций сортировки** отображается критерий **Отгрузка — услуга перевозчика — Авиа**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="3fd93-549">Сортировка остальных контейнеров</span><span class="sxs-lookup"><span data-stu-id="3fd93-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="3fd93-550">На мобильном устройстве выполните вход на склад *62*, используя код пользователя, созданный для этого сценария (или идентификатор пользователя существующего пользователя демонстрационных данных).</span><span class="sxs-lookup"><span data-stu-id="3fd93-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="3fd93-551">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3fd93-552">В меню **Исходящее** выберите **Сборка палет**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="3fd93-553">В поле **Грузоместо/контейнер** введите второй код контейнера, связанный с заказом на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="3fd93-554">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-554">Select **OK**.</span></span> <span data-ttu-id="3fd93-555">Поскольку шаблон сортировки настроен на автоматическую сортировку, а позиция сортировки с подходящими критериями уже существует, пользователь автоматически направляется в правильную позицию сортировки.</span><span class="sxs-lookup"><span data-stu-id="3fd93-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="3fd93-556">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-556">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-557">Подтвердите код позиции сортировки, чтобы указать, что запасы находятся в правильной позиции.</span><span class="sxs-lookup"><span data-stu-id="3fd93-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="3fd93-558">В поле **Код позиции сортировки** введите *SP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="3fd93-559">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-559">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-560">Работа завершается для второго контейнера из заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="3fd93-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="3fd93-561">Теперь выполните сортировку оставшихся контейнеров из заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="3fd93-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="3fd93-562">В поле **Грузоместо/контейнер** введите код контейнера для контейнера из заказа на продажу 2, который содержит номенклатуру *A0001*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="3fd93-563">Так как услуга перевозчика отличается, выводится запрос на ввод новой позиции сортировки и назначение грузоместа этой позиции.</span><span class="sxs-lookup"><span data-stu-id="3fd93-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="3fd93-564">Используйте позицию сортировки *SP02* и грузоместо *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="3fd93-565">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-565">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-566">Подтвердите позицию сортировки, введя *SP02* в поле **Код позиции сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="3fd93-567">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-567">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-568">Работа над контейнером завершена.</span><span class="sxs-lookup"><span data-stu-id="3fd93-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="3fd93-569">В поле **Грузоместо/контейнер** введите код контейнера для оставшегося контейнера из заказа на продажу 2, который содержит номенклатуру *A0002*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="3fd93-570">Так как услуга перевозчика совпадает с услугой перевозчика для заказа на продажу 1, в системе отображается существующая позиция сортировки, соответствующая критериям.</span><span class="sxs-lookup"><span data-stu-id="3fd93-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="3fd93-571">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-571">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-572">Подтвердите позицию сортировки, введя *SP01* в поле **Код позиции сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="3fd93-573">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-573">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-574">Работа над контейнером завершена.</span><span class="sxs-lookup"><span data-stu-id="3fd93-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="3fd93-575">Закрытие позиций исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="3fd93-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="3fd93-576">После сортировки всех запасов необходимо закрыть позицию, прежде чем можно будет создать работу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="3fd93-577">Будет создана работа комплектации сортированных запасов, чтобы переместить запасы к двери отсека.</span><span class="sxs-lookup"><span data-stu-id="3fd93-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="3fd93-578">Закрытие позиции с мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="3fd93-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="3fd93-579">На мобильном устройстве выполните вход на склад *62*, используя код пользователя, созданный для этого сценария (или идентификатор пользователя существующего пользователя демонстрационных данных).</span><span class="sxs-lookup"><span data-stu-id="3fd93-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="3fd93-580">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3fd93-581">В меню **Исходящее** выберите **Сборка палет**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="3fd93-582">В поле **Грузоместо/Контейнер** введите код контейнера, который был отсортирован для позиции сортировки *SP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="3fd93-583">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-583">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-584">Появится следующее сообщение: "Контейнер уже отсортирован в позиции SP01.</span><span class="sxs-lookup"><span data-stu-id="3fd93-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="3fd93-585">Закрыть позицию?"</span><span class="sxs-lookup"><span data-stu-id="3fd93-585">Close the position?"</span></span> <span data-ttu-id="3fd93-586">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-586">Select **Close**.</span></span>

    <span data-ttu-id="3fd93-587">Работа завершена.</span><span class="sxs-lookup"><span data-stu-id="3fd93-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="3fd93-588">Закрытие позиции из назначений позиций исходящей сортировки</span><span class="sxs-lookup"><span data-stu-id="3fd93-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="3fd93-589">Перейдите в раздел **Управление складом \> Упаковка и контейнеризация \> Назначение позиций исходящей сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="3fd93-590">В левом столбце выберите **SP02**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="3fd93-591">Эта строка позиции исходящей сортировки является той, которая будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="3fd93-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="3fd93-592">В области действий выберите **Закрыть позицию**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="3fd93-593">Запись позиции сортировки закрывается и больше не отображается.</span><span class="sxs-lookup"><span data-stu-id="3fd93-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="3fd93-594">Чтобы показать все записи закрытых позиций, установите флажок **Показать закрытые**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="3fd93-595">Комплектация отсортированных запасов</span><span class="sxs-lookup"><span data-stu-id="3fd93-595">Sorted inventory picking</span></span>

<span data-ttu-id="3fd93-596">Необходимо выполнить отсортированную работу по комплектации запасов.</span><span class="sxs-lookup"><span data-stu-id="3fd93-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="3fd93-597">После ее завершения запасы будут скомплектованы по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="3fd93-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="3fd93-598">В этот момент применяются все остальные складские процессы.</span><span class="sxs-lookup"><span data-stu-id="3fd93-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="3fd93-599">На мобильном устройстве выполните вход на склад *62*, используя код пользователя, созданный для этого сценария (или идентификатор пользователя существующего пользователя демонстрационных данных).</span><span class="sxs-lookup"><span data-stu-id="3fd93-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="3fd93-600">В главном меню выберите **Исходящее**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3fd93-601">В меню **Исходящие** выберите **Загрузить из сортировки**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="3fd93-602">Введите код целевого грузоместа из первой позиции сортировки, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="3fd93-603">Задайте в поле **Код** значение *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="3fd93-604">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-604">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-605">На странице **Комплектация отсортированных запасов: комплектация** отображается работа комплектации, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="3fd93-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="3fd93-606">Выберите комплектацию из местонахождения *СОРТИРОВКА* и целевое грузоместо *PLP01*, которое содержит несколько номенклатур и количество *3*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="3fd93-607">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-607">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-608">На странице **Комплектация отсортированных запасов: размещение** отображается работа размещения, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="3fd93-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="3fd93-609">Разместите в местонахождении *Дверь отсека* и целевом грузоместе *PLP01*, которое содержит несколько номенклатур и количество *3*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="3fd93-610">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-610">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-611">Работа завершена.</span><span class="sxs-lookup"><span data-stu-id="3fd93-611">Work is completed.</span></span>

1. <span data-ttu-id="3fd93-612">Введите код целевого грузоместа из второй позиции сортировки, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="3fd93-613">Задайте в поле **Код** значение *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="3fd93-614">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-614">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-615">На странице **Комплектация отсортированных запасов: комплектация** отображается работа комплектации, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="3fd93-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="3fd93-616">Выберите комплектацию из местонахождения *СОРТИРОВКА* и целевое грузоместо *PLP02*, которое содержит несколько номенклатур и количество *1*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="3fd93-617">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-617">Select **OK**.</span></span>
1. <span data-ttu-id="3fd93-618">На странице **Комплектация отсортированных запасов: размещение** отображается работа размещения, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="3fd93-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="3fd93-619">Разместите в местонахождении *Дверь отсека* и целевом грузоместе *PLP02*, которое содержит несколько номенклатур и количество *1*.</span><span class="sxs-lookup"><span data-stu-id="3fd93-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="3fd93-620">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3fd93-620">Select **OK**.</span></span>

    <span data-ttu-id="3fd93-621">Работа завершена.</span><span class="sxs-lookup"><span data-stu-id="3fd93-621">Work is completed.</span></span>

<span data-ttu-id="3fd93-622">Начиная с этого момента применяются все остальные складские процессы.</span><span class="sxs-lookup"><span data-stu-id="3fd93-622">From this point forward, all other warehouse processes apply.</span></span>
