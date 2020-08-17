---
title: Модуль карты
description: В этом разделе описываются модули карты, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647030"
---
# <a name="map-module"></a><span data-ttu-id="5dc24-103">Модуль карты</span><span class="sxs-lookup"><span data-stu-id="5dc24-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5dc24-104">В этом разделе описываются модули карты, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5dc24-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5dc24-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5dc24-105">Overview</span></span>

<span data-ttu-id="5dc24-106">Модуль карты показывает местоположение магазинов на интерактивной карте, которая отображается с помощью [веб-элемента управления Карт Bing V8](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="5dc24-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="5dc24-107">Требуется ключ API карт Bing, который должен быть добавлен на страницу общих параметров в центральном офисе Commerce.</span><span class="sxs-lookup"><span data-stu-id="5dc24-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="5dc24-108">Модули карты предоставляют различающиеся представления, такие как дорога, с воздуха и улицы, которые пользователи могут выбрать для просмотра местоположений на карте.</span><span class="sxs-lookup"><span data-stu-id="5dc24-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="5dc24-109">Они также позволяют выполнять такие действия, как масштабирование и использование местоположения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dc24-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="5dc24-110">Модуль карты взаимодействует с модулем выбора магазина, чтобы определить географическое местоположение магазинов, которые должны быть визуализированы на карте.</span><span class="sxs-lookup"><span data-stu-id="5dc24-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="5dc24-111">Модули выбора магазина и карты взаимодействуют, когда пользователь выбирает магазин в одном из этих модулей на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="5dc24-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="5dc24-112">Модули карты могут быть расширены для других сценариев, помимо взаимодействия с модулями выбора магазина.</span><span class="sxs-lookup"><span data-stu-id="5dc24-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="5dc24-113">Однако необходимо выполнить настройку модуля.</span><span class="sxs-lookup"><span data-stu-id="5dc24-113">However, module customization is required.</span></span>

<span data-ttu-id="5dc24-114">Модуль карты был введен в Commerce версии 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="5dc24-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="5dc24-115">На следующем рисунке показан пример модуля карты, используемый на странице местоположений магазинов.</span><span class="sxs-lookup"><span data-stu-id="5dc24-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Пример модуля выбора магазина](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="5dc24-117">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="5dc24-117">Module properties</span></span>

| <span data-ttu-id="5dc24-118">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="5dc24-118">Property name</span></span>             | <span data-ttu-id="5dc24-119">значение</span><span class="sxs-lookup"><span data-stu-id="5dc24-119">Value</span></span>                 | <span data-ttu-id="5dc24-120">описание</span><span class="sxs-lookup"><span data-stu-id="5dc24-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5dc24-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5dc24-121">Heading</span></span> | <span data-ttu-id="5dc24-122">Текст</span><span class="sxs-lookup"><span data-stu-id="5dc24-122">Text</span></span> | <span data-ttu-id="5dc24-123">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="5dc24-123">The heading for the module.</span></span> |
| <span data-ttu-id="5dc24-124">Параметры кнопки: значок по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5dc24-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="5dc24-125">Изображение</span><span class="sxs-lookup"><span data-stu-id="5dc24-125">Image</span></span> | <span data-ttu-id="5dc24-126">Изображение символа канцелярской кнопки для использования в магазинах, отображаемых на карте.</span><span class="sxs-lookup"><span data-stu-id="5dc24-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="5dc24-127">Параметры кнопки: значок "Активно"</span><span class="sxs-lookup"><span data-stu-id="5dc24-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="5dc24-128">Изображение</span><span class="sxs-lookup"><span data-stu-id="5dc24-128">Image</span></span> | <span data-ttu-id="5dc24-129">Изображение символа канцелярской кнопки для использования для магазина, отображаемого на карте.</span><span class="sxs-lookup"><span data-stu-id="5dc24-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="5dc24-130">Параметры кнопки: цвет значка по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5dc24-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="5dc24-131">Символьная строка</span><span class="sxs-lookup"><span data-stu-id="5dc24-131">Character string</span></span> | <span data-ttu-id="5dc24-132">Текстовое или шестнадцатеричное значение цвета символа кнопки.</span><span class="sxs-lookup"><span data-stu-id="5dc24-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="5dc24-133">Параметры кнопки: цвет значка "Активно"</span><span class="sxs-lookup"><span data-stu-id="5dc24-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="5dc24-134">Символьная строка</span><span class="sxs-lookup"><span data-stu-id="5dc24-134">Character string</span></span> | <span data-ttu-id="5dc24-135">Текстовое или шестнадцатеричное значение цвета выбранных символов кнопки.</span><span class="sxs-lookup"><span data-stu-id="5dc24-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="5dc24-136">Показать индекс</span><span class="sxs-lookup"><span data-stu-id="5dc24-136">Show index</span></span> | <span data-ttu-id="5dc24-137">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5dc24-137">**True** or **False**</span></span> | <span data-ttu-id="5dc24-138">Если это свойство имеет значение **Истина**, то у каждого символа кнопки, который обозначает магазин, будет показан индекс.</span><span class="sxs-lookup"><span data-stu-id="5dc24-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="5dc24-139">Этот индекс будет соответствовать индексу в представлении списка, который отображается в модуле выбора магазина.</span><span class="sxs-lookup"><span data-stu-id="5dc24-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="5dc24-140">Добавление разрешенных URL-адресов для сопоставления в директивы политики безопасности содержимого сайта</span><span class="sxs-lookup"><span data-stu-id="5dc24-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="5dc24-141">Для взаимодействия модуля карты с Картами Bing необходимо убедиться, что следующие URL-адреса сопоставления разрешены (также называются "список разрешенных") в политике безопасности содержимого сайта (CSP).</span><span class="sxs-lookup"><span data-stu-id="5dc24-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="5dc24-142">Эта настройка выполняется в построителе сайтов Commerce путем добавления разрешенных URL-адресов в различные директивы CSP для сайта (например, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="5dc24-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="5dc24-143">Дополнительные сведения см. в разделе [Политика безопасности содержимого](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="5dc24-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="5dc24-144">В директиву **connect-src** добавьте **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="5dc24-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="5dc24-145">В директиву **img-src**, добавьте **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="5dc24-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="5dc24-146">В директиву **script-src** добавьте **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="5dc24-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="5dc24-147">В директиву **script style-src** добавьте **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="5dc24-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="5dc24-148">Добавление модуля карты на страницу</span><span class="sxs-lookup"><span data-stu-id="5dc24-148">Add a map module to a page</span></span>

<span data-ttu-id="5dc24-149">Подробные сведения о настройке модуля карты на странице см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5dc24-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="5dc24-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5dc24-150">Additional resources</span></span>

[<span data-ttu-id="5dc24-151">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="5dc24-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5dc24-152">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="5dc24-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5dc24-153">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="5dc24-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5dc24-154">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="5dc24-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="5dc24-155">Управление картами Bing для вашей организации</span><span class="sxs-lookup"><span data-stu-id="5dc24-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="5dc24-156">Веб-элемент управления Карт Bing V8</span><span class="sxs-lookup"><span data-stu-id="5dc24-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
