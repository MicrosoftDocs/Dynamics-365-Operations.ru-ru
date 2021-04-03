---
title: Настройка склада
description: В этом разделе описывается, как настроить склад для использования с новым каналом в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477642"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="44cfe-103">Настройка складов</span><span class="sxs-lookup"><span data-stu-id="44cfe-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="44cfe-104">В этом разделе описывается, как настроить склад для использования с новым каналом в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="44cfe-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="44cfe-105">Для каждого канала Commerce необходим настроенный склад, который должен быть связан с ним.</span><span class="sxs-lookup"><span data-stu-id="44cfe-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="44cfe-106">Следующие процедуры обеспечивают минимальную конфигурацию, необходимую для настройки склада для канала Commerce.</span><span class="sxs-lookup"><span data-stu-id="44cfe-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="44cfe-107">Дополнительные сведения о настройке склада см. в [Обзор управления складом](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="44cfe-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="44cfe-108">Настройка сайта склада</span><span class="sxs-lookup"><span data-stu-id="44cfe-108">Configure a warehouse site</span></span>

<span data-ttu-id="44cfe-109">Перед настройкой склада необходимо настроить сайт склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="44cfe-110">Чтобы настроить сайт склада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44cfe-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="44cfe-111">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="44cfe-112">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="44cfe-113">В поле **Сайт** введите значение.</span><span class="sxs-lookup"><span data-stu-id="44cfe-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="44cfe-114">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="44cfe-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="44cfe-115">В разделе **Общее** задайте соответствующий **Часовой пояс**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="44cfe-116">В разделе **Адреса** введите адрес.</span><span class="sxs-lookup"><span data-stu-id="44cfe-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="44cfe-117">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="44cfe-118">На следующем рисунке показан пример сайта склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-118">The following image shows an example warehouse site.</span></span>

![Пример: сайт склада](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="44cfe-120">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="44cfe-120">Set up a warehouse</span></span>

<span data-ttu-id="44cfe-121">Чтобы настроить склад, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="44cfe-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="44cfe-122">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="44cfe-123">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="44cfe-124">В поле **Склад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="44cfe-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="44cfe-125">Если это сопоставление 1:1 с магазином, можно воспользоваться именем магазина или названием регионального центра распределения.</span><span class="sxs-lookup"><span data-stu-id="44cfe-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="44cfe-126">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="44cfe-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="44cfe-127">В раскрывающемся списке **Сайт** выберите сайт склада, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="44cfe-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="44cfe-128">В поле **Тип** выберите **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="44cfe-129">Если требуется настроить **Карантинный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Карантин**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="44cfe-130">Если требуется настроить **Транзитный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Транзит**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="44cfe-131">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="44cfe-132">Настройка складских проходов</span><span class="sxs-lookup"><span data-stu-id="44cfe-132">Set up inventory aisles</span></span>

<span data-ttu-id="44cfe-133">Чтобы настроить складские проходы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44cfe-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="44cfe-134">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Настройка местонахождения \> Складские проходы**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="44cfe-135">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="44cfe-136">В раскрывающемся списке **Склад** выберите склад, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="44cfe-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="44cfe-137">В поле **Проход** введите имя (например, "Def").</span><span class="sxs-lookup"><span data-stu-id="44cfe-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="44cfe-138">В поле **Имя** введите имя (например, "Default aisle").</span><span class="sxs-lookup"><span data-stu-id="44cfe-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="44cfe-139">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="44cfe-140">Настройка местонахождений запасов склада</span><span class="sxs-lookup"><span data-stu-id="44cfe-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="44cfe-141">Чтобы настроить местонахождения запасов склада для стандартных, поврежденных и возвращенных запасов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44cfe-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="44cfe-142">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="44cfe-143">Выберите созданный ранее склад.</span><span class="sxs-lookup"><span data-stu-id="44cfe-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="44cfe-144">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="44cfe-145">На панели операций выберите **Склад**, а затем выберите **Место хранения**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="44cfe-146">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-146">On the action pane, select **New**.</span></span> <span data-ttu-id="44cfe-147">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="44cfe-148">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="44cfe-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="44cfe-149">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="44cfe-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="44cfe-150">В поле **Местонахождение** введите имя склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="44cfe-151">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="44cfe-152">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="44cfe-153">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="44cfe-154">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="44cfe-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="44cfe-155">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="44cfe-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="44cfe-156">В поле **Местоположение** введите "повреждено".</span><span class="sxs-lookup"><span data-stu-id="44cfe-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="44cfe-157">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="44cfe-158">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="44cfe-159">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="44cfe-160">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="44cfe-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="44cfe-161">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="44cfe-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="44cfe-162">В поле **Местоположение** введите "возврат".</span><span class="sxs-lookup"><span data-stu-id="44cfe-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="44cfe-163">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="44cfe-164">На следующем рисунке показана настройка местонахождения запасов склада "Сан-Франциско".</span><span class="sxs-lookup"><span data-stu-id="44cfe-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Пример настройки местонахождения запасов](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="44cfe-166">Завершение настройки склада</span><span class="sxs-lookup"><span data-stu-id="44cfe-166">Complete warehouse setup</span></span>

<span data-ttu-id="44cfe-167">Чтобы завершить настройку склада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44cfe-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="44cfe-168">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="44cfe-169">Выберите созданный ранее склад.</span><span class="sxs-lookup"><span data-stu-id="44cfe-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="44cfe-170">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="44cfe-171">В **Управление запасами и складами**:</span><span class="sxs-lookup"><span data-stu-id="44cfe-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="44cfe-172">Задайте для **Ячейка прихода по умолчанию** ячейку по умолчанию, созданную выше.</span><span class="sxs-lookup"><span data-stu-id="44cfe-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="44cfe-173">Выберите для **Ячейка расхода по умолчанию** ячейку по умолчанию, созданную выше.</span><span class="sxs-lookup"><span data-stu-id="44cfe-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="44cfe-174">В разделе **Адреса** введите адрес склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="44cfe-175">В разделе **Розница**:</span><span class="sxs-lookup"><span data-stu-id="44cfe-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="44cfe-176">В поле **Расположение возврата по умолчанию** введите ранее созданное местонахождение возврата.</span><span class="sxs-lookup"><span data-stu-id="44cfe-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="44cfe-177">Задайте для **Магазин** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="44cfe-178">Задайте **Вес** как **1,00**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="44cfe-179">В поле **Аналитики хранения** введите ранее созданное местонахождение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="44cfe-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="44cfe-180">В разделе **Склад** установите для параметра **Физический отрицательный запас** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="44cfe-181">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44cfe-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="44cfe-182">На следующем рисунке показаны данные для настроенного склада.</span><span class="sxs-lookup"><span data-stu-id="44cfe-182">The following image shows details for a configured warehouse.</span></span>

![Пример настроенного склада](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="44cfe-184">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44cfe-184">Additional resources</span></span>

[<span data-ttu-id="44cfe-185">Обзор управления складом</span><span class="sxs-lookup"><span data-stu-id="44cfe-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="44cfe-186">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="44cfe-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="44cfe-187">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="44cfe-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="44cfe-188">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="44cfe-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="44cfe-189">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="44cfe-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="44cfe-190">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="44cfe-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
