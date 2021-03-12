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
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993661"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="2d971-103">Настройка складов</span><span class="sxs-lookup"><span data-stu-id="2d971-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2d971-104">В этом разделе описывается, как настроить склад для использования с новым каналом в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d971-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2d971-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2d971-105">Overview</span></span>

<span data-ttu-id="2d971-106">Для каждого канала Commerce необходим настроенный склад, который должен быть связан с ним.</span><span class="sxs-lookup"><span data-stu-id="2d971-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="2d971-107">Следующие процедуры обеспечивают минимальную конфигурацию, необходимую для настройки склада для канала Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d971-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="2d971-108">Дополнительные сведения о настройке склада см. в [Обзор управления складом](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2d971-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="2d971-109">Настройка сайта склада</span><span class="sxs-lookup"><span data-stu-id="2d971-109">Configure a warehouse site</span></span>

<span data-ttu-id="2d971-110">Перед настройкой склада необходимо настроить сайт склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="2d971-111">Чтобы настроить сайт склада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d971-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="2d971-112">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="2d971-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="2d971-113">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2d971-114">В поле **Сайт** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2d971-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="2d971-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2d971-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2d971-116">В разделе **Общее** задайте соответствующий **Часовой пояс**.</span><span class="sxs-lookup"><span data-stu-id="2d971-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="2d971-117">В разделе **Адреса** введите адрес.</span><span class="sxs-lookup"><span data-stu-id="2d971-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="2d971-118">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="2d971-119">На следующем рисунке показан пример сайта склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-119">The following image shows an example warehouse site.</span></span>

![Пример: сайт склада](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="2d971-121">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="2d971-121">Set up a warehouse</span></span>

<span data-ttu-id="2d971-122">Чтобы настроить склад, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="2d971-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="2d971-123">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="2d971-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="2d971-124">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2d971-125">В поле **Склад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2d971-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="2d971-126">Если это сопоставление 1:1 с магазином, можно воспользоваться именем магазина или названием регионального центра распределения.</span><span class="sxs-lookup"><span data-stu-id="2d971-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="2d971-127">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2d971-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2d971-128">В раскрывающемся списке **Сайт** выберите сайт склада, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="2d971-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="2d971-129">В поле **Тип** выберите **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="2d971-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="2d971-130">Если требуется настроить **Карантинный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Карантин**.</span><span class="sxs-lookup"><span data-stu-id="2d971-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="2d971-131">Если требуется настроить **Транзитный склад**, сначала необходимо выполнить следующие действия для создания дополнительного склада, где для этого **Тип** устанавливается значение **Транзит**.</span><span class="sxs-lookup"><span data-stu-id="2d971-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="2d971-132">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="2d971-133">Настройка складских проходов</span><span class="sxs-lookup"><span data-stu-id="2d971-133">Set up inventory aisles</span></span>

<span data-ttu-id="2d971-134">Чтобы настроить складские проходы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d971-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="2d971-135">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Настройка местонахождения \> Складские проходы**.</span><span class="sxs-lookup"><span data-stu-id="2d971-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="2d971-136">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2d971-137">В раскрывающемся списке **Склад** выберите склад, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="2d971-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="2d971-138">В поле **Проход** введите имя (например, "Def").</span><span class="sxs-lookup"><span data-stu-id="2d971-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="2d971-139">В поле **Имя** введите имя (например, "Default aisle").</span><span class="sxs-lookup"><span data-stu-id="2d971-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="2d971-140">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="2d971-141">Настройка местонахождений запасов склада</span><span class="sxs-lookup"><span data-stu-id="2d971-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="2d971-142">Чтобы настроить местонахождения запасов склада для стандартных, поврежденных и возвращенных запасов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d971-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="2d971-143">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="2d971-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="2d971-144">Выберите созданный ранее склад.</span><span class="sxs-lookup"><span data-stu-id="2d971-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="2d971-145">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="2d971-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="2d971-146">На панели операций выберите **Склад**, а затем выберите **Место хранения**.</span><span class="sxs-lookup"><span data-stu-id="2d971-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="2d971-147">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-147">On the action pane, select **New**.</span></span> <span data-ttu-id="2d971-148">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="2d971-149">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="2d971-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="2d971-150">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="2d971-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="2d971-151">В поле **Местонахождение** введите имя склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="2d971-152">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="2d971-153">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="2d971-154">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="2d971-155">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="2d971-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="2d971-156">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="2d971-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="2d971-157">В поле **Местоположение** введите "повреждено".</span><span class="sxs-lookup"><span data-stu-id="2d971-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="2d971-158">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="2d971-159">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2d971-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="2d971-160">В раскрывающемся списке **Склад** должно быть значение по умолчанию для нового склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="2d971-161">В поле **Проход** введите название прохода, который был указан ранее.</span><span class="sxs-lookup"><span data-stu-id="2d971-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="2d971-162">Задайте для **Ручное изменение** **Да**</span><span class="sxs-lookup"><span data-stu-id="2d971-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="2d971-163">В поле **Местоположение** введите "возврат".</span><span class="sxs-lookup"><span data-stu-id="2d971-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="2d971-164">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="2d971-165">На следующем рисунке показана настройка местонахождения запасов склада "Сан-Франциско".</span><span class="sxs-lookup"><span data-stu-id="2d971-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Пример настройки местонахождения запасов](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="2d971-167">Завершение настройки склада</span><span class="sxs-lookup"><span data-stu-id="2d971-167">Complete warehouse setup</span></span>

<span data-ttu-id="2d971-168">Чтобы завершить настройку склада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2d971-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="2d971-169">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Склады**.</span><span class="sxs-lookup"><span data-stu-id="2d971-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="2d971-170">Выберите созданный ранее склад.</span><span class="sxs-lookup"><span data-stu-id="2d971-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="2d971-171">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="2d971-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="2d971-172">В **Управление запасами и складами**:</span><span class="sxs-lookup"><span data-stu-id="2d971-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="2d971-173">Задайте для **Ячейка прихода по умолчанию** ячейку по умолчанию, созданную выше.</span><span class="sxs-lookup"><span data-stu-id="2d971-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="2d971-174">Выберите для **Ячейка расхода по умолчанию** ячейку по умолчанию, созданную выше.</span><span class="sxs-lookup"><span data-stu-id="2d971-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="2d971-175">В разделе **Адреса** введите адрес склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="2d971-176">В разделе **Розница**:</span><span class="sxs-lookup"><span data-stu-id="2d971-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="2d971-177">В поле **Расположение возврата по умолчанию** введите ранее созданное местонахождение возврата.</span><span class="sxs-lookup"><span data-stu-id="2d971-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="2d971-178">Задайте для **Магазин** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2d971-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="2d971-179">Задайте **Вес** как **1,00**.</span><span class="sxs-lookup"><span data-stu-id="2d971-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="2d971-180">В поле **Аналитики хранения** введите ранее созданное местонахождение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d971-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="2d971-181">В разделе **Склад** установите для параметра **Физический отрицательный запас** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2d971-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="2d971-182">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2d971-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="2d971-183">На следующем рисунке показаны данные для настроенного склада.</span><span class="sxs-lookup"><span data-stu-id="2d971-183">The following image shows details for a configured warehouse.</span></span>

![Пример настроенного склада](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="2d971-185">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d971-185">Additional resources</span></span>

[<span data-ttu-id="2d971-186">Обзор управления складом</span><span class="sxs-lookup"><span data-stu-id="2d971-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2d971-187">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="2d971-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2d971-188">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="2d971-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="2d971-189">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="2d971-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="2d971-190">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="2d971-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="2d971-191">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d971-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





