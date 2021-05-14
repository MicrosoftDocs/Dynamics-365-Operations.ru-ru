---
title: Применение настроек запасов
description: В этой теме описываются настройки запасов и описывается порядок их применения в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dd3db0039525c18521ad6a42b2f281976b7b236a
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937418"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="1d151-103">Применение настроек запасов</span><span class="sxs-lookup"><span data-stu-id="1d151-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1d151-104">В этой теме описываются настройки запасов и описывается порядок их применения в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d151-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1d151-105">Параметры запасов определяют, следует ли проверять запасы перед добавлением продуктов в корзину.</span><span class="sxs-lookup"><span data-stu-id="1d151-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="1d151-106">Они также определяют связанные с запасами рекламные сообщения, такие как "В наличии" и "Осталось несколько".</span><span class="sxs-lookup"><span data-stu-id="1d151-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="1d151-107">Эти параметры гарантируют, что продукт невозможно купить, если его нет на складе.</span><span class="sxs-lookup"><span data-stu-id="1d151-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="1d151-108">Dynamics 365 Commerce предоставляет оценки доступности продуктов в наличии.</span><span class="sxs-lookup"><span data-stu-id="1d151-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="1d151-109">Сведения о том, как рассчитываются оценки доступности в наличии, см. в разделе [Расчет наличия запасов для розничных каналов](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="1d151-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="1d151-110">В построителе сайтов Commerce пороговые значения и диапазоны запасов могут быть определены для продукта или категории.</span><span class="sxs-lookup"><span data-stu-id="1d151-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="1d151-111">Они определяют, могут ли запасы классифицироваться как "в наличии", "осталось мало" или "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="1d151-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="1d151-112">Подробности см. в разделе [Настройка буферов запасов и уровней запасов](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1d151-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1d151-113">Поддержка пороговых значений и диапазонов запасов доступна в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="1d151-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="1d151-114">Параметры запасов</span><span class="sxs-lookup"><span data-stu-id="1d151-114">Inventory settings</span></span>

<span data-ttu-id="1d151-115">В Commerce параметры запасов определяются в **Параметры сайта \> Расширения \> Управление запасами** в построителе сайтов.</span><span class="sxs-lookup"><span data-stu-id="1d151-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="1d151-116">Есть пять параметров запасов, один из которых является устаревшим:</span><span class="sxs-lookup"><span data-stu-id="1d151-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="1d151-117">**Включить проверку запасов в приложении** — этот параметр включает проверку запасов продукта.</span><span class="sxs-lookup"><span data-stu-id="1d151-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="1d151-118">Модули поля покупки, корзины и получения в магазине затем проверяют запасы продукта и позволят добавить продукт в корзину только в том случае, если он доступен в запасах.</span><span class="sxs-lookup"><span data-stu-id="1d151-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="1d151-119">**На основе уровня запасов** — этот параметр определяет, как будут рассчитываться уровни запасов.</span><span class="sxs-lookup"><span data-stu-id="1d151-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="1d151-120">Доступны значения **Доступное общее количество**, **Физическая доступность** и **Пороговое значение "нет на складе"**.</span><span class="sxs-lookup"><span data-stu-id="1d151-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="1d151-121">В Commerce пороговые значения и диапазоны запасов могут быть определены для каждого продукта и категории.</span><span class="sxs-lookup"><span data-stu-id="1d151-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="1d151-122">API запасов возвращают сведения о запасах продуктов для обоих свойств **Доступное общее количество** и **Физическая доступность**.</span><span class="sxs-lookup"><span data-stu-id="1d151-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="1d151-123">Розничный продавец определяет, должно ли значение **Доступное общее количество** или **Физическая доступность** использоваться для определения количества запасов и соответствующих диапазонов для статусов "на складе" и "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="1d151-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="1d151-124">Значение **Пороговое значение "нет на складе"** параметра **На основе уровня запасов** устарело и не используется.</span><span class="sxs-lookup"><span data-stu-id="1d151-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="1d151-125">Когда оно установлено, количество запасов определяется на основе результатов **Общее доступное количество**, но пороговое значение определяется в соответствии с числовым параметром **Пороговое значение "нет на складе"**, которая описывается дальше.</span><span class="sxs-lookup"><span data-stu-id="1d151-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="1d151-126">Это пороговое значение применяется ко всем продуктам на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="1d151-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="1d151-127">Если запасы меньше порогового значения, продукт считается отсутствующим на складе.</span><span class="sxs-lookup"><span data-stu-id="1d151-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="1d151-128">В противном случае считается "в наличии".</span><span class="sxs-lookup"><span data-stu-id="1d151-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="1d151-129">Возможности значения **Пороговое значение "нет на складе"** ограничены, и поэтому не рекомендуется использовать его в версии 10.0.12 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1d151-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="1d151-130">**Уровень запасов для нескольких складов** — эта настройка активирует возможность расчета уровня запасов по умолчанию для склада или для нескольких складов.</span><span class="sxs-lookup"><span data-stu-id="1d151-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="1d151-131">Параметр **На основе отдельного склада** используется для расчета уровней складских запасов на основе склада по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d151-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="1d151-132">Кроме того, сайт электронной коммерции может указывать на несколько складов для облегчения выполнения работ.</span><span class="sxs-lookup"><span data-stu-id="1d151-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="1d151-133">В этом случае для параметра **На основе агрегирования для складов отгрузки и отправки** используется для указания наличия запасов.</span><span class="sxs-lookup"><span data-stu-id="1d151-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="1d151-134">Например, когда клиент приобретает номенклатуру и выбирает "отгрузка" в качестве способа доставки, номенклатуру можно отгрузить с любого склада в группе выполнения, имеющей доступные запасы.</span><span class="sxs-lookup"><span data-stu-id="1d151-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="1d151-135">Страница сведения о продукте (PDP) будет показывать сообщение "в наличии" для отгрузки, если какой-либо доступный склад отгрузки в группе выполнения содержит запасы.</span><span class="sxs-lookup"><span data-stu-id="1d151-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="1d151-136">Параметр **Уровень запасов для нескольких складов** доступен в Commerce версии 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="1d151-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="1d151-137">Если выполняется обновление с более ранней версии Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="1d151-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1d151-138">Дополнительные инструкции см. в разделе [Обновления пакета SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="1d151-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="1d151-139">**Диапазоны запасов** — этот параметр определяет диапазоны запасов, для которых показывается сообщение для модулей на сайте.</span><span class="sxs-lookup"><span data-stu-id="1d151-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="1d151-140">Оно применимо только в том случае, если значение **Общее доступное количество** или значение **Физическая доступность** выбрано для параметра **На основе уровня запасов**.</span><span class="sxs-lookup"><span data-stu-id="1d151-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="1d151-141">Доступны значения **Все**, **Мало и нет на складе** и **Нет на складе**.</span><span class="sxs-lookup"><span data-stu-id="1d151-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="1d151-142">Когда выбрано значение **Все**, будут отображаться сообщения для всех диапазонов запасов, начиная с "в наличии" (сообщение "Доступно") до "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="1d151-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="1d151-143">Когда выбрано значение **Мало и нет на складе**, будут отображаться сообщения для всех диапазонов запасов кроме "в наличии" (сообщение "Доступно").</span><span class="sxs-lookup"><span data-stu-id="1d151-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="1d151-144">Если выбрано значение **Нет на складе**, будет отображаться только сообщение "Нет на складе".</span><span class="sxs-lookup"><span data-stu-id="1d151-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="1d151-145">**Пороговое значение "нет на складе"** — этот старый числовой параметр вступит в силу только в том случае, если значение **Пороговое значение "нет на складе"** выбрано для параметр **На основе уровня запасов**.</span><span class="sxs-lookup"><span data-stu-id="1d151-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="1d151-146">Эти параметры доступны в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="1d151-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="1d151-147">Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="1d151-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1d151-148">Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="1d151-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="1d151-149">Модули, в которых используются параметры запасов</span><span class="sxs-lookup"><span data-stu-id="1d151-149">Modules that use inventory settings</span></span>

<span data-ttu-id="1d151-150">Модули поля покупки, списка желаемого, выбора магазина, корзины и значка корзины используют параметры запасов для отображения диапазонов и сообщений запасов.</span><span class="sxs-lookup"><span data-stu-id="1d151-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="1d151-151">В примере на следующем рисунке PDP показывает сообщение "в наличии" ("доступно").</span><span class="sxs-lookup"><span data-stu-id="1d151-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![Пример модуля PDP с информационным сообщением "в наличии"](./media/pdp-InStock.png)

<span data-ttu-id="1d151-153">В примере на следующем рисунке PDP показывает сообщение "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="1d151-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![Пример модуля PDP с информационным сообщением "нет на складе"](./media/pdp-outofstock.png)

<span data-ttu-id="1d151-155&quot;>В примере на следующем рисунке PDP корзина показывает сообщение &quot;в наличии&quot; (&quot;доступно").</span><span class="sxs-lookup"><span data-stu-id="1d151-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Пример модуля корзины с информационным сообщением "в наличии"](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="1d151-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d151-157">Additional resources</span></span>

[<span data-ttu-id="1d151-158">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="1d151-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1d151-159">Настройка буферов запасов и уровней запасов</span><span class="sxs-lookup"><span data-stu-id="1d151-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="1d151-160">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="1d151-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1d151-161">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="1d151-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1d151-162">Страницы и модули управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="1d151-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="1d151-163">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="1d151-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="1d151-164">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="1d151-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
