--- 
title: "Настойка упаковки вручную (только версии от февраля и мая 2016 г.)"
description: "Процесс упаковки позволяет утвердить и упаковать продукты в контейнеры."
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7e776a08ec2adc48b77c86c16e1f291e524a8d00
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="fade5-103">Настойка упаковки вручную (только версии от февраля и мая 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="fade5-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fade5-104">Процесс упаковки позволяет утвердить и упаковать продукты в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="fade5-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="fade5-105">В ходе этого процесса работники склада комплектуют продукты из мест хранения и перемещают их на станции упаковки, где они выполняют проверку количества и типов номенклатур и назначают их соответствующим контейнерам.</span><span class="sxs-lookup"><span data-stu-id="fade5-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="fade5-106">Когда контейнер полностью упакован, его можно закрыть и переместить в дебаркадеры отгрузки; продукты готовы к отгрузке.</span><span class="sxs-lookup"><span data-stu-id="fade5-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="fade5-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="fade5-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="fade5-108">Настройка профилей местонахождений</span><span class="sxs-lookup"><span data-stu-id="fade5-108">Set up location profiles</span></span>
1. <span data-ttu-id="fade5-109">Перейдите в раздел "Управление складом" > "Настройка" > "Склад" > "Профили местонахождения".</span><span class="sxs-lookup"><span data-stu-id="fade5-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="fade5-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fade5-110">Click New.</span></span>
    * <span data-ttu-id="fade5-111">Профиль местонахождения используется для станций упаковки и содержит информацию и правила для местонахождения.</span><span class="sxs-lookup"><span data-stu-id="fade5-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="fade5-112">В поле "Код профиля местонахождения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="fade5-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fade5-114">В поле "Формат местонахождения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="fade5-115">В поле "Тип местоположения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="fade5-116">Выберите значение "Да" в поле "Разрешить смешанные номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="fade5-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="fade5-117">Выберите значение "Да" в поле "Разрешить смешанные статусы запасов".</span><span class="sxs-lookup"><span data-stu-id="fade5-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="fade5-118">Выберите значение "Да" в поле "Переопределить правила для пакетных дней".</span><span class="sxs-lookup"><span data-stu-id="fade5-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="fade5-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fade5-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="fade5-120">Настройка параметров управления складом</span><span class="sxs-lookup"><span data-stu-id="fade5-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="fade5-121">Перейдите в раздел "Управление складом" > "Настройка" > "Параметры управления складом".</span><span class="sxs-lookup"><span data-stu-id="fade5-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="fade5-122">Перейдите на вкладку "Упаковка".</span><span class="sxs-lookup"><span data-stu-id="fade5-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="fade5-123">В поле "Код профиля для местонахождения упаковки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="fade5-124">Выберите профиль местонахождения, который необходимо использовать для упаковки.</span><span class="sxs-lookup"><span data-stu-id="fade5-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="fade5-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fade5-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="fade5-126">Настройка типов контейнеров</span><span class="sxs-lookup"><span data-stu-id="fade5-126">Set up container types</span></span>
1. <span data-ttu-id="fade5-127">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Типы контейнеров".</span><span class="sxs-lookup"><span data-stu-id="fade5-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="fade5-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fade5-128">Click New.</span></span>
    * <span data-ttu-id="fade5-129">Можно определить типы контейнеров для использования.</span><span class="sxs-lookup"><span data-stu-id="fade5-129">You can define the types of containers to use.</span></span> <span data-ttu-id="fade5-130">Можно указать физические аналитики контейнера, включая вес тары, максимальный вес, максимальный объем, длину, ширину и вес.</span><span class="sxs-lookup"><span data-stu-id="fade5-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="fade5-131">Атрибуты — это пользовательские поля, которые позволяют добавить дополнительные аналитики для типа контейнера.</span><span class="sxs-lookup"><span data-stu-id="fade5-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="fade5-132">В поле "Код типа контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="fade5-133">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fade5-134">В поле "Вес тары" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="fade5-135">В поле "Максимальный вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="fade5-136">В поле "Объем" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="fade5-137">В поле "Длина" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="fade5-138">В поле "Ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="fade5-139">В поле "Высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="fade5-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="fade5-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fade5-140">Click Save.</span></span>
12. <span data-ttu-id="fade5-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fade5-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="fade5-142">Настройка профилей упаковки</span><span class="sxs-lookup"><span data-stu-id="fade5-142">Set up packing profiles</span></span>
1. <span data-ttu-id="fade5-143">Перейдите в раздел "Управление складом" > "Настройка" > "Упаковка" > "Профили упаковки".</span><span class="sxs-lookup"><span data-stu-id="fade5-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="fade5-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fade5-144">Click New.</span></span>
3. <span data-ttu-id="fade5-145">В поле "Код профиля упаковки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="fade5-146">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fade5-147">В поле "Код профиля закрытия контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="fade5-148">Код профиля закрытия контейнера необязателен и является профилем закрытия контейнера по умолчанию для этого профиля упаковки.</span><span class="sxs-lookup"><span data-stu-id="fade5-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="fade5-149">В поле "Режим кода контейнера" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="fade5-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="fade5-150">Этот параметр определяет, будет ли код контейнера создаваться автоматически при создании контейнера или будет ли код контейнера создаваться вручную.</span><span class="sxs-lookup"><span data-stu-id="fade5-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="fade5-151">В поле "Тип контейнера" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="fade5-152">Тип контейнера будет использоваться по умолчанию при создании нового контейнера.</span><span class="sxs-lookup"><span data-stu-id="fade5-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="fade5-153">Установите флажок "Автоматически создавать контейнер при закрытии контейнера".</span><span class="sxs-lookup"><span data-stu-id="fade5-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="fade5-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fade5-154">Click Save.</span></span>
10. <span data-ttu-id="fade5-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fade5-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="fade5-156">Настройка профилей закрытия контейнера</span><span class="sxs-lookup"><span data-stu-id="fade5-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="fade5-157">Перейдите в раздел "Управление складом" > "Настройка" > "Контейнеры" > "Профили закрытия контейнеров".</span><span class="sxs-lookup"><span data-stu-id="fade5-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="fade5-158">Профили закрытия контейнера определяют, что происходит, когда контейнер закрывается.</span><span class="sxs-lookup"><span data-stu-id="fade5-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="fade5-159">Можно настроить несколько профилей закрытия контейнера.</span><span class="sxs-lookup"><span data-stu-id="fade5-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="fade5-160">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fade5-160">Click New.</span></span>
3. <span data-ttu-id="fade5-161">В поле "Код профиля закрытия контейнера" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="fade5-162">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fade5-163">В поле "Манифест по" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="fade5-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="fade5-164">Определите, будет ли декларирование выполняться при закрытии контейнера или при подтверждении отгрузки.</span><span class="sxs-lookup"><span data-stu-id="fade5-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="fade5-165">Обратите внимание, что для декларирования требуется управление транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="fade5-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="fade5-166">Декларирование необходимо выполнять в механизмах транспортировки для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="fade5-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="fade5-167">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="fade5-168">В поле "Местонахождение по умолчанию для конечной отгрузки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="fade5-169">Это будет местонахождение, в которое будут перемещены продукты после закрытия контейнеров.</span><span class="sxs-lookup"><span data-stu-id="fade5-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="fade5-170">Это местонахождение должно иметь профиль местонахождения, определенный в параметрах склада.</span><span class="sxs-lookup"><span data-stu-id="fade5-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="fade5-171">В поле "Единица веса" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fade5-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="fade5-172">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fade5-172">Click Save.</span></span>


