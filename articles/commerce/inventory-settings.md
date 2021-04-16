---
title: Применение настроек запасов
description: В этой теме описываются настройки запасов и описывается порядок их применения в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798897"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="cc475-103">Применение настроек запасов</span><span class="sxs-lookup"><span data-stu-id="cc475-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc475-104">В этой теме описываются настройки запасов и описывается порядок их применения в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc475-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cc475-105">Параметры запасов определяют, следует ли проверять запасы перед добавлением продуктов в корзину.</span><span class="sxs-lookup"><span data-stu-id="cc475-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="cc475-106">Они также определяют связанные с запасами рекламные сообщения, такие как "В наличии" и "Осталось несколько".</span><span class="sxs-lookup"><span data-stu-id="cc475-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="cc475-107">Эти параметры гарантируют, что продукт невозможно купить, если его нет на складе.</span><span class="sxs-lookup"><span data-stu-id="cc475-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="cc475-108">Dynamics 365 Commerce предоставляет оценки доступности продуктов в наличии.</span><span class="sxs-lookup"><span data-stu-id="cc475-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="cc475-109">Сведения о том, как рассчитываются оценки доступности в наличии, см. в разделе [Расчет наличия запасов для розничных каналов](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="cc475-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="cc475-110">В построителе сайтов Commerce пороговые значения и диапазоны запасов могут быть определены для продукта или категории.</span><span class="sxs-lookup"><span data-stu-id="cc475-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="cc475-111">Они определяют, могут ли запасы классифицироваться как "в наличии", "осталось мало" или "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="cc475-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="cc475-112">Подробности см. в разделе [Настройка буферов запасов и уровней запасов](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cc475-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cc475-113">Поддержка пороговых значений и диапазонов запасов доступна в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="cc475-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="cc475-114">Параметры запасов</span><span class="sxs-lookup"><span data-stu-id="cc475-114">Inventory settings</span></span>

<span data-ttu-id="cc475-115">В Commerce параметры запасов определяются в **Параметры сайта \> Расширения \> Управление запасами** в построителе сайтов.</span><span class="sxs-lookup"><span data-stu-id="cc475-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="cc475-116">Есть четыре параметра запасов, один из которых является устаревшим:</span><span class="sxs-lookup"><span data-stu-id="cc475-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="cc475-117">**Включить проверку запасов в приложении** — этот параметр включает проверку запасов продукта.</span><span class="sxs-lookup"><span data-stu-id="cc475-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="cc475-118">Модули поля покупки, корзины и получения в магазине затем проверяют запасы продукта и позволят добавить продукт в корзину только в том случае, если он доступен в запасах.</span><span class="sxs-lookup"><span data-stu-id="cc475-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="cc475-119">**На основе уровня запасов** — этот параметр определяет, как будут рассчитываться уровни запасов.</span><span class="sxs-lookup"><span data-stu-id="cc475-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="cc475-120">Доступны значения **Доступное общее количество**, **Физическая доступность** и **Пороговое значение "нет на складе"**.</span><span class="sxs-lookup"><span data-stu-id="cc475-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="cc475-121">В Commerce пороговые значения и диапазоны запасов могут быть определены для каждого продукта и категории.</span><span class="sxs-lookup"><span data-stu-id="cc475-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="cc475-122">API запасов возвращают сведения о запасах продуктов для обоих свойств **Доступное общее количество** и **Физическая доступность**.</span><span class="sxs-lookup"><span data-stu-id="cc475-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="cc475-123">Розничный продавец определяет, должно ли значение **Доступное общее количество** или **Физическая доступность** использоваться для определения количества запасов и соответствующих диапазонов для статусов "на складе" и "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="cc475-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="cc475-124">Значение **Пороговое значение "нет на складе"** параметра **На основе уровня запасов** устарело и не используется.</span><span class="sxs-lookup"><span data-stu-id="cc475-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="cc475-125">Когда оно установлено, количество запасов определяется на основе результатов **Общее доступное количество**, но пороговое значение определяется в соответствии с числовым параметром **Пороговое значение "нет на складе"**, которая описывается дальше.</span><span class="sxs-lookup"><span data-stu-id="cc475-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="cc475-126">Это пороговое значение применяется ко всем продуктам на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="cc475-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="cc475-127">Если запасы меньше порогового значения, продукт считается отсутствующим на складе.</span><span class="sxs-lookup"><span data-stu-id="cc475-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="cc475-128">В противном случае считается "в наличии".</span><span class="sxs-lookup"><span data-stu-id="cc475-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="cc475-129">Возможности значения **Пороговое значение "нет на складе"** ограничены, и поэтому не рекомендуется использовать его в версии 10.0.12 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="cc475-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="cc475-130">**Диапазоны запасов** — этот параметр определяет диапазоны запасов, для которых показывается сообщение для модулей на сайте.</span><span class="sxs-lookup"><span data-stu-id="cc475-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="cc475-131">Оно применимо только в том случае, если значение **Общее доступное количество** или значение **Физическая доступность** выбрано для параметра **На основе уровня запасов**.</span><span class="sxs-lookup"><span data-stu-id="cc475-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="cc475-132">Доступны значения **Все**, **Мало и нет на складе** и **Нет на складе**.</span><span class="sxs-lookup"><span data-stu-id="cc475-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="cc475-133">Когда выбрано значение **Все**, будут отображаться сообщения для всех диапазонов запасов, начиная с "в наличии" (сообщение "Доступно") до "нет на складе".</span><span class="sxs-lookup"><span data-stu-id="cc475-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="cc475-134">Когда выбрано значение **Мало и нет на складе**, будут отображаться сообщения для всех диапазонов запасов кроме "в наличии" (сообщение "Доступно").</span><span class="sxs-lookup"><span data-stu-id="cc475-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="cc475-135">Если выбрано значение **Нет на складе**, будет отображаться только сообщение "Нет на складе".</span><span class="sxs-lookup"><span data-stu-id="cc475-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="cc475-136">**Пороговое значение "нет на складе"** — этот старый числовой параметр вступит в силу только в том случае, если значение **Пороговое значение "нет на складе"** выбрано для параметр **На основе уровня запасов**.</span><span class="sxs-lookup"><span data-stu-id="cc475-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="cc475-137">Эти параметры доступны в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="cc475-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="cc475-138">Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="cc475-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="cc475-139">Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="cc475-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="cc475-140">Модули, в которых используются параметры запасов</span><span class="sxs-lookup"><span data-stu-id="cc475-140">Modules that use inventory settings</span></span>

<span data-ttu-id="cc475-141">Модули поля покупки, списка желаемого, выбора магазина, корзины и значка корзины используют параметры запасов для отображения диапазонов и сообщений запасов.</span><span class="sxs-lookup"><span data-stu-id="cc475-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="cc475-142">На следующем рисунке показан пример страницы сведений о продукте (PDP), на которой отображается сообщение "в наличии" ("Доступно").</span><span class="sxs-lookup"><span data-stu-id="cc475-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Пример модуля PDP с информационным сообщением "в наличии"](./media/pdp-InStock.png)

<span data-ttu-id="cc475-144">На следующем рисунке показан пример PDP, на которой отображается сообщение "Нет на складе".</span><span class="sxs-lookup"><span data-stu-id="cc475-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Пример модуля PDP с информационным сообщением "нет на складе"](./media/pdp-outofstock.png)

<span data-ttu-id="cc475-146&quot;>На следующем рисунке показан пример корзины, где отображается сообщение &quot;в наличии&quot; (&quot;Доступно").</span><span class="sxs-lookup"><span data-stu-id="cc475-146">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Пример модуля корзины с информационным сообщением "в наличии"](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="cc475-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc475-148">Additional resources</span></span>

[<span data-ttu-id="cc475-149">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="cc475-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cc475-150">Настройка буферов запасов и уровней запасов</span><span class="sxs-lookup"><span data-stu-id="cc475-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="cc475-151">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="cc475-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cc475-152">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="cc475-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cc475-153">Страницы и модули управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="cc475-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="cc475-154">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="cc475-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="cc475-155">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="cc475-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
