---
title: Применение настроек единицы измерения
description: В этой теме описываются настройки единицы измерения и описывается порядок их применения в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2c5750ae506978dfac842eebf4ba6036322bdd7f
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937614"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="e5790-103">Применение настроек единицы измерения</span><span class="sxs-lookup"><span data-stu-id="e5790-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e5790-104">В этой теме описываются настройки единицы измерения и описывается порядок их применения в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e5790-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e5790-105">Продукт может продаваться в различных единицах измерения, таких как "штука", "пара", "десяток".</span><span class="sxs-lookup"><span data-stu-id="e5790-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="e5790-106">В Commerce Headquarters единица измерения продажи может быть определена для продукта и показана на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="e5790-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="e5790-107">Например, если розничный продавец продает продукт как отдельно, так и десятками, доступные единицы измерения могут отображаться вместе с другими сведениями о продукте.</span><span class="sxs-lookup"><span data-stu-id="e5790-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="e5790-108">В примере на следующем рисунке для продукта в Commerce Headquarters сконфигурирована единица измерения **шт** (штука).</span><span class="sxs-lookup"><span data-stu-id="e5790-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Пример продукта, сконфигурированного с единицей измерения в модуле Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="e5790-110">Поддержка применения и отображения единицы измерения доступна в Commerce версии 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e5790-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="e5790-111">Настройки единицы измерения</span><span class="sxs-lookup"><span data-stu-id="e5790-111">Unit of measure settings</span></span>

<span data-ttu-id="e5790-112">Параметры отображения единицы измерения определяются в конструкторе сайтов Commerce в **Параметры сайта \> Расширения \> Отображение единиц измерения для продуктов**.</span><span class="sxs-lookup"><span data-stu-id="e5790-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="e5790-113">Имеется три поддерживаемые настройки:</span><span class="sxs-lookup"><span data-stu-id="e5790-113">There are three supported settings:</span></span>

- <span data-ttu-id="e5790-114">**Не отображать** — если этот параметр выбран, на сайте электронной коммерции не будет отображаться единица измерения для продукта.</span><span class="sxs-lookup"><span data-stu-id="e5790-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="e5790-115">Такое поведение является поведением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5790-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="e5790-116">**Отображение во время приобретения продукта** — когда выбран этот параметр, единица измерения отображается на страницах сведений о продукте, корзины, оформления заказа, журнала заказов и сведений о заказах.</span><span class="sxs-lookup"><span data-stu-id="e5790-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="e5790-117">**Отображение при просмотре товаров и при покупке** — если выбран этот параметр, единица измерения отображается на страницах покупки продукта, а также во время просмотра продуктов.</span><span class="sxs-lookup"><span data-stu-id="e5790-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="e5790-118">В рамках такого поведения единицы измерения отображаются в результатах поиска и модулях коллекции продуктов.</span><span class="sxs-lookup"><span data-stu-id="e5790-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5790-119">Параметры отображения единиц измерения доступны в Commerce в версии 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e5790-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="e5790-120">Если выполняется обновление с более ранней версии Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="e5790-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="e5790-121">Дополнительные инструкции см. в разделе [Обновления пакета SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="e5790-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="e5790-122">Модули, в которых используется настройка единиц измерения</span><span class="sxs-lookup"><span data-stu-id="e5790-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="e5790-123">Модули, в которых используются параметры единицы измерения, включают в себя модули поля покупки, списка желаемого, корзины, значка корзины, контейнера результатов поиска, коллекции продуктов, оформления заказа и сведений о заказах.</span><span class="sxs-lookup"><span data-stu-id="e5790-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="e5790-124">В примере на следующем рисунке страница сведения о продукте (PDP) содержит единицу измерения (**шт**) для продукта.</span><span class="sxs-lookup"><span data-stu-id="e5790-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Пример PDP, отображающей единицу измерения](./media/Productunit-PDP.png)

<span data-ttu-id="e5790-126">В примере на следующем рисунке модуль коллекции продуктов содержит единицу измерения (**шт**) для продукта.</span><span class="sxs-lookup"><span data-stu-id="e5790-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Пример модуля коллекции продуктов, отображающего единицу измерения](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="e5790-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5790-128">Additional resources</span></span>

[<span data-ttu-id="e5790-129">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="e5790-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e5790-130">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="e5790-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e5790-131">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="e5790-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e5790-132">Страницы и модули управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="e5790-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="e5790-133">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="e5790-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
