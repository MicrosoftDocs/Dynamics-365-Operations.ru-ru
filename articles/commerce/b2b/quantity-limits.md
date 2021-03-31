---
title: Настройка лимитов количества продуктов для сайтов электронной коммерции B2B
description: В этом разделе описывается, как настроить лимиты количества продуктов для сайтов электронной коммерции бизнес-бизнес (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211185"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="41364-103">Настройка лимитов количества продуктов для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="41364-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41364-104">В этом разделе описывается, как настроить лимиты количества продуктов для сайтов электронной коммерции бизнес-бизнес (B2B).</span><span class="sxs-lookup"><span data-stu-id="41364-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="41364-105">У большинства продуктов есть единица измерения, определяющая их группировку.</span><span class="sxs-lookup"><span data-stu-id="41364-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="41364-106">Группировка влияет на то, как могут продаваться продукты.</span><span class="sxs-lookup"><span data-stu-id="41364-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="41364-107">У некоторых продуктов может быть дополнительная группировка по количеству.</span><span class="sxs-lookup"><span data-stu-id="41364-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="41364-108">Эта группировка определяет, могут ли продукты продаваться как отдельные единицы или как кратные, а также имеется ли минимальное или максимальное количество в заказе, которое должно быть соблюдено.</span><span class="sxs-lookup"><span data-stu-id="41364-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="41364-109">Функция ограничения количества обеспечивает применение минимального, максимального, кратного и стандартного количеств, настроенных в Microsoft Dynamics 365 Commerce (в настройках заказа по умолчанию или в настройках конструктора сайтов Commerce), к заказам клиентов, размещенных на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="41364-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="41364-110">Ограничения количества продукта в настоящее время не поддерживаются для POS-терминалов и центров обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="41364-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="41364-111">Многие компании розничной торговли предоставляют возможность заказов клиента (также называемых специальными заказами) для удовлетворения требований разных продуктов и требований выполнения.</span><span class="sxs-lookup"><span data-stu-id="41364-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="41364-112">Вот некоторые типовые сценарии:</span><span class="sxs-lookup"><span data-stu-id="41364-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="41364-113">Клиент хочет, чтобы продукты некоторых вариантов продавались в кратных количествах.</span><span class="sxs-lookup"><span data-stu-id="41364-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="41364-114">Клиент хочет забрать продукты из магазина или местоположения, отличных от магазина или местоположения, где клиент приобрел эти продукты.</span><span class="sxs-lookup"><span data-stu-id="41364-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="41364-115">Однако стандарты упаковки для магазинов отличаются от стандартов упаковки для распределения продаж через Интернет.</span><span class="sxs-lookup"><span data-stu-id="41364-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="41364-116">Клиент хочет купить ограниченный выпуск продукта с максимальным ограничением количества, которое можно приобрести.</span><span class="sxs-lookup"><span data-stu-id="41364-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="41364-117">Включение функции настроек заказа по умолчанию в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="41364-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="41364-118">Прежде чем можно будет задать пределы количества продуктов, в Commerce headquarters должна быть включена функция настройки заказов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41364-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="41364-119">Чтобы включить функцию настроек заказа по умолчанию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41364-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="41364-120">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="41364-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="41364-121">Найдите и выберите функцию **Поддержка настроек сайта и заказа по умолчанию в клиентском заказе**.</span><span class="sxs-lookup"><span data-stu-id="41364-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="41364-122">В нижней части правой области выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="41364-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="41364-123">Определение настроек количества</span><span class="sxs-lookup"><span data-stu-id="41364-123">Define quantity settings</span></span> 

<span data-ttu-id="41364-124">Можно определить параметры количества на странице **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="41364-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="41364-125">Для определения параметров количества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41364-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="41364-126">Перейдите в раздел **Retail и Commerce \> Продукты и категории \> Выпущенные продукты по категориям**.</span><span class="sxs-lookup"><span data-stu-id="41364-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="41364-127">Выберите выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="41364-127">Select a released product.</span></span>
1. <span data-ttu-id="41364-128">На панели действий на вкладке **Управление запасами** в группе **Настройки заказа** выберите **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="41364-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="41364-129">На странице **Параметры заказа по умолчанию** на экспресс-вкладке **Заказ на продажу** в разделе **Количество продажи** задайте количества продажи продуктов:</span><span class="sxs-lookup"><span data-stu-id="41364-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="41364-130">**Кратное** — количество, кратное которому можно купить продукт.</span><span class="sxs-lookup"><span data-stu-id="41364-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="41364-131">**Минимальное количество заказа** — минимальное количество продуктов, которое необходимо купить.</span><span class="sxs-lookup"><span data-stu-id="41364-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="41364-132">**Максимальное количество заказа** — максимальное количество продуктов, которое можно купить.</span><span class="sxs-lookup"><span data-stu-id="41364-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="41364-133">**Стандартное количество заказа** — количество по умолчанию, которое автоматически вводится при выборе продукта.</span><span class="sxs-lookup"><span data-stu-id="41364-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="41364-134">Включение функции ограничения количества заказа B2B в конструкторе сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="41364-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="41364-135">Чтобы включить функцию ограничения количества заказа B2B в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41364-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="41364-136">Перейдите к разделу **Параметры сайта \> Расширения**</span><span class="sxs-lookup"><span data-stu-id="41364-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="41364-137">В области **Включить пределы количества заказов** выберите **Включены для клиентов B2B** в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="41364-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="41364-138">Обновленные параметры конструктора сайтов вступят в силу только после обновления файла app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="41364-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="41364-139">Дополнительные сведения см. в разделе [Обновления пакета SDK и библиотеки модулей](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="41364-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41364-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41364-140">Additional resources</span></span>

[<span data-ttu-id="41364-141">Настройка сайта электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="41364-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="41364-142">Создание иерархий моделирования организации для организаций B2B</span><span class="sxs-lookup"><span data-stu-id="41364-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="41364-143">Управление пользователями деловых партнеров на сайтах электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="41364-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="41364-144">Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="41364-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]