---
title: Применение параметров дисплея для аналитик продукта
description: В этой теме описываются параметры отображения для аналитик продукта и описывается, как применять их в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117243"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="2c7e2-103">Применение параметров дисплея для аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="2c7e2-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2c7e2-104">В этой теме описываются параметры отображения для аналитик продукта и описывается, как применять их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c7e2-105">Dynamics 365 Commerce поддерживает аналитики размера, стиля и цвета для различения вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="2c7e2-106">Аналитики обычно отображаются как текстовые значения, такие как "Маленький", "Средний" и "Большой" для размеров, "Черный" и "Коричневый" для цветов.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="2c7e2-107">Однако если продукт поддерживает множество вариантов, может быть сложно просматривать варианты продукта, поскольку для просмотра изображения каждого варианта требуется выбрать несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="2c7e2-108">Для облегчения просмотра вариантов продуктов в выпуске версии 10.0.20 Commerce могут использоваться изображения и шестнадцатеричные коды (HEX), позволяющие отображать аналитики как образцы.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="2c7e2-109">В конструкторе сайтов Commerce параметры аналитики определяются в разделе **Параметры сайта \> Расширения \> Параметры аналитик**.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="2c7e2-110">На следующем рисунке показан пример настроек аналитик в конструкторе сайтов.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Пример настроек сайта в конструкторе сайтов Commerce](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="2c7e2-112">Доступны два параметра аналитики:</span><span class="sxs-lookup"><span data-stu-id="2c7e2-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="2c7e2-113">**Аналитики для отображения как изображения** — определяет, какие аналитики будут показаны как образцы на страницах сайта электронной коммерции, таких как страницы сведений о продукте (PDP) и страницы списка результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="2c7e2-114">Любые комбинации аналитик цвета, размера и стиля могут отображаться как образцы.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="2c7e2-115">Если аналитика выбрана для отображения в качестве образца, отрисовка модуля Commerce будет искать доступную конфигурацию образца шестнадцатеричного кода.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="2c7e2-116">Если шестнадцатеричный код не настроен, системная логика будет искать конфигурацию образца URL-адреса изображения.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="2c7e2-117">Если не настроен ни шестнадцатеричный код, ни URL-адрес изображения, отображается текст.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="2c7e2-118">На следующем рисунке показан пример, в котором страница PDP сайта электронной коммерции включает образцы цвета и размера.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="2c7e2-119">В этом примере шестнадцатеричный код сконфигурирован для аналитики цвета.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="2c7e2-120">Поэтому образцы отображаются как цвета.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="2c7e2-121">Однако ни шестнадцатеричный код, ни URL-адрес изображения не настроен для аналитики размера.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="2c7e2-122">Поэтому отображается текст.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-122">Therefore, text is shown.</span></span>

    ![Пример аналитики цвета, отображаемой как образцы на странице сведений о продукте на сайте электронной коммерции](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="2c7e2-124">**Аналитики, отображаемые в карточке продукта** — укажите, какие аналитики должны отображаться в карточках продуктов, которые отображаются в списках и на страницах списков.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="2c7e2-125">Если аналитика может отображаться на карточке продукта, эта настройка должна быть активирована для этой аналитики.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="2c7e2-126">Настройка **Аналитики для отображения в виде изображений** также должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="2c7e2-127">Поведение выбора образца для карточек продуктов оптимизировано для аналитики цвета.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="2c7e2-128">Для других аналитик для настройки поведения выбора образца может потребоваться расширение просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="2c7e2-129">На следующем рисунке показан пример, в котором страница списка на сайте электронной коммерции содержит карточки продукта, содержащие образцы цветов.</span><span class="sxs-lookup"><span data-stu-id="2c7e2-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Пример аналитики цвета, отображаемой как образцы на странице списка электронной коммерции](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="2c7e2-131">Сведения о настройке аналитик продукта для их отображения в качестве образцов на страницах сайта см. в разделе [Настройка значений аналитики продукта для отображения в виде образцов](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="2c7e2-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c7e2-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c7e2-132">Additional resources</span></span>

[<span data-ttu-id="2c7e2-133">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="2c7e2-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c7e2-134">Модуль результатов поиска</span><span class="sxs-lookup"><span data-stu-id="2c7e2-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="2c7e2-135">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="2c7e2-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2c7e2-136">Настройка значений аналитики продукта для отображения в виде образцов</span><span class="sxs-lookup"><span data-stu-id="2c7e2-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
