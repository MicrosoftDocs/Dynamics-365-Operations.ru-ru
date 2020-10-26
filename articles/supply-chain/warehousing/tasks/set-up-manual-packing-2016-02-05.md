---
title: Настройка ручной упаковки (февраль 2016 г. и май 2016 г.)
description: Процесс упаковки позволяет утвердить и упаковать продукты в контейнеры.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa3ef51a7b6fa553e5919befdab6818755deea52
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978419"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="d05ca-103">Настройка ручной упаковки (февраль 2016 г. и май 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="d05ca-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d05ca-104">Процесс упаковки позволяет утвердить и упаковать продукты в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="d05ca-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="d05ca-105">В ходе этого процесса работники склада комплектуют продукты из мест хранения и перемещают их на станции упаковки, где они выполняют проверку количества и типов номенклатур и назначают их соответствующим контейнерам.</span><span class="sxs-lookup"><span data-stu-id="d05ca-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="d05ca-106">Когда контейнер полностью упакован, его можно закрыть и переместить в дебаркадеры отгрузки; продукты готовы к отгрузке.</span><span class="sxs-lookup"><span data-stu-id="d05ca-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="d05ca-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="d05ca-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="d05ca-108">Эта процедура относится только к версиям Dynamics 365 for Operations от февраля 2016 и мая 2016.</span><span class="sxs-lookup"><span data-stu-id="d05ca-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="d05ca-109">Настройка профилей местонахождений</span><span class="sxs-lookup"><span data-stu-id="d05ca-109">Set up location profiles</span></span>
1. <span data-ttu-id="d05ca-110">Перейдите в раздел "Управление складом" > "Настройка" > "Склад" > "Профили местонахождения".</span><span class="sxs-lookup"><span data-stu-id="d05ca-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="d05ca-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d05ca-111">Click New.</span></span>
    * <span data-ttu-id="d05ca-112">Профиль местонахождения используется для станций упаковки и содержит информацию и правила для местонахождения.</span><span class="sxs-lookup"><span data-stu-id="d05ca-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="d05ca-113">В поле "Код профиля местонахождения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="d05ca-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d05ca-115">В поле "Формат местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="d05ca-116">В поле "Тип местоположения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="d05ca-117">Выберите значение "Да" в поле "Разрешить смешанные номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="d05ca-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d05ca-118">Выберите значение "Да" в поле "Разрешить смешанные статусы запасов".</span><span class="sxs-lookup"><span data-stu-id="d05ca-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d05ca-119">Выберите значение "Да" в поле "Переопределить правила для пакетных дней".</span><span class="sxs-lookup"><span data-stu-id="d05ca-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="d05ca-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d05ca-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d05ca-121">Настройка параметров управления складом</span><span class="sxs-lookup"><span data-stu-id="d05ca-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="d05ca-122">Перейдите в раздел "Управление складом" > "Настройка" > "Параметры управления складом".</span><span class="sxs-lookup"><span data-stu-id="d05ca-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d05ca-123">Перейдите на вкладку "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="d05ca-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="d05ca-124">В поле "Код профиля для местонахождения упаковки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="d05ca-125">Выберите профиль местонахождения, который необходимо использовать для упаковки.</span><span class="sxs-lookup"><span data-stu-id="d05ca-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="d05ca-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d05ca-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="d05ca-127">Настройка типов контейнеров</span><span class="sxs-lookup"><span data-stu-id="d05ca-127">Set up container types</span></span>
1. <span data-ttu-id="d05ca-128">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="d05ca-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="d05ca-129">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d05ca-129">Click New.</span></span>
    * <span data-ttu-id="d05ca-130">Можно определить типы контейнеров для использования.</span><span class="sxs-lookup"><span data-stu-id="d05ca-130">You can define the types of containers to use.</span></span> <span data-ttu-id="d05ca-131">Можно указать физические аналитики контейнера, включая вес тары, максимальный вес, максимальный объем, длину, ширину и вес.</span><span class="sxs-lookup"><span data-stu-id="d05ca-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="d05ca-132">Атрибуты — это пользовательские поля, которые позволяют добавить дополнительные аналитики для типа контейнера.</span><span class="sxs-lookup"><span data-stu-id="d05ca-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="d05ca-133">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="d05ca-134">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d05ca-135">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="d05ca-136">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="d05ca-137">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="d05ca-138">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="d05ca-139">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="d05ca-140">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="d05ca-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="d05ca-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d05ca-141">Click Save.</span></span>
12. <span data-ttu-id="d05ca-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d05ca-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="d05ca-143">Настройка профилей упаковки</span><span class="sxs-lookup"><span data-stu-id="d05ca-143">Set up packing profiles</span></span>
1. <span data-ttu-id="d05ca-144">Перейдите в раздел "Управление складом" > "Настройка" > "Упаковка" > "Профили упаковки".</span><span class="sxs-lookup"><span data-stu-id="d05ca-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="d05ca-145">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d05ca-145">Click New.</span></span>
3. <span data-ttu-id="d05ca-146">В поле "Код профиля упаковки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d05ca-147">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d05ca-148">В поле "Код профиля закрытия контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d05ca-149">Код профиля закрытия контейнера необязателен и является профилем закрытия контейнера по умолчанию для этого профиля упаковки.</span><span class="sxs-lookup"><span data-stu-id="d05ca-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="d05ca-150">В поле "Режим кода контейнера" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="d05ca-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="d05ca-151">Этот параметр определяет, будет ли код контейнера создаваться автоматически при создании контейнера или будет ли код контейнера создаваться вручную.</span><span class="sxs-lookup"><span data-stu-id="d05ca-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="d05ca-152">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="d05ca-153">Тип контейнера будет использоваться по умолчанию при создании нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="d05ca-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="d05ca-154">Установите флажок "Автоматически создавать контейнер при закрытии контейнера".</span><span class="sxs-lookup"><span data-stu-id="d05ca-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="d05ca-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d05ca-155">Click Save.</span></span>
10. <span data-ttu-id="d05ca-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d05ca-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="d05ca-157">Настройка профилей закрытия контейнера</span><span class="sxs-lookup"><span data-stu-id="d05ca-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="d05ca-158">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Профили закрытия контейнеров".</span><span class="sxs-lookup"><span data-stu-id="d05ca-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="d05ca-159">Профили закрытия контейнера определяют, что происходит, когда контейнер закрывается.</span><span class="sxs-lookup"><span data-stu-id="d05ca-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="d05ca-160">Можно настроить несколько профилей закрытия контейнера.</span><span class="sxs-lookup"><span data-stu-id="d05ca-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="d05ca-161">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d05ca-161">Click New.</span></span>
3. <span data-ttu-id="d05ca-162">В поле "Код профиля закрытия контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d05ca-163">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d05ca-164">В поле "Манифест по" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="d05ca-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="d05ca-165">Определите, будет ли декларирование выполняться при закрытии контейнера или при подтверждении отгрузки.</span><span class="sxs-lookup"><span data-stu-id="d05ca-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="d05ca-166">Обратите внимание, что для декларирования требуется управление транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="d05ca-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="d05ca-167">Декларирование необходимо выполнять в механизмах транспортировки для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="d05ca-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="d05ca-168">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d05ca-169">В поле "Местонахождение по умолчанию для конечной отгрузки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="d05ca-170">Это будет местонахождение, в которое будут перемещены продукты после закрытия контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d05ca-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="d05ca-171">Это местонахождение должно иметь профиль местонахождения, определенный в параметрах склада.</span><span class="sxs-lookup"><span data-stu-id="d05ca-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="d05ca-172">В поле "Единица веса" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d05ca-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="d05ca-173">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d05ca-173">Click Save.</span></span>

