---
title: Модуль карты
description: В этом разделе описываются модули карты, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794195"
---
# <a name="map-module"></a><span data-ttu-id="47f66-103">Модуль карты</span><span class="sxs-lookup"><span data-stu-id="47f66-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="47f66-104">В этом разделе описываются модули карты, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="47f66-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47f66-105">Модуль карты показывает местоположение магазинов на интерактивной карте, которая отображается с помощью [веб-элемента управления Карт Bing V8](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="47f66-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="47f66-106">Требуется ключ API карт Bing, который должен быть добавлен на страницу общих параметров в центральном офисе Commerce.</span><span class="sxs-lookup"><span data-stu-id="47f66-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="47f66-107">Модули карты предоставляют различающиеся представления, такие как дорога, с воздуха и улицы, которые пользователи могут выбрать для просмотра местоположений на карте.</span><span class="sxs-lookup"><span data-stu-id="47f66-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="47f66-108">Они также позволяют выполнять такие действия, как масштабирование и использование местоположения пользователя.</span><span class="sxs-lookup"><span data-stu-id="47f66-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="47f66-109">Модуль карты взаимодействует с модулем выбора магазина, чтобы определить географическое местоположение магазинов, которые должны быть визуализированы на карте.</span><span class="sxs-lookup"><span data-stu-id="47f66-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="47f66-110">Модули выбора магазина и карты взаимодействуют, когда пользователь выбирает магазин в одном из этих модулей на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="47f66-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="47f66-111">Модули карты могут быть расширены для других сценариев, помимо взаимодействия с модулями выбора магазина.</span><span class="sxs-lookup"><span data-stu-id="47f66-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="47f66-112">Однако необходимо выполнить настройку модуля.</span><span class="sxs-lookup"><span data-stu-id="47f66-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="47f66-113">Модуль карты доступен в выпуске Dynamics 365 Commerce 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="47f66-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="47f66-114">На следующем рисунке показан пример модуля карты, используемый на странице местоположений магазинов.</span><span class="sxs-lookup"><span data-stu-id="47f66-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Пример модуля выбора магазина](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="47f66-116">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="47f66-116">Module properties</span></span>

| <span data-ttu-id="47f66-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="47f66-117">Property name</span></span>             | <span data-ttu-id="47f66-118">значение</span><span class="sxs-lookup"><span data-stu-id="47f66-118">Value</span></span>                 | <span data-ttu-id="47f66-119">описание</span><span class="sxs-lookup"><span data-stu-id="47f66-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="47f66-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47f66-120">Heading</span></span> | <span data-ttu-id="47f66-121">Текст</span><span class="sxs-lookup"><span data-stu-id="47f66-121">Text</span></span> | <span data-ttu-id="47f66-122">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="47f66-122">The heading for the module.</span></span> |
| <span data-ttu-id="47f66-123">Параметры кнопки: значок по умолчанию</span><span class="sxs-lookup"><span data-stu-id="47f66-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="47f66-124">Изображение</span><span class="sxs-lookup"><span data-stu-id="47f66-124">Image</span></span> | <span data-ttu-id="47f66-125">Изображение символа канцелярской кнопки для использования в магазинах, отображаемых на карте.</span><span class="sxs-lookup"><span data-stu-id="47f66-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="47f66-126">Параметры кнопки: значок "Активно"</span><span class="sxs-lookup"><span data-stu-id="47f66-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="47f66-127">Изображение</span><span class="sxs-lookup"><span data-stu-id="47f66-127">Image</span></span> | <span data-ttu-id="47f66-128">Изображение символа канцелярской кнопки для использования для магазина, отображаемого на карте.</span><span class="sxs-lookup"><span data-stu-id="47f66-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="47f66-129">Параметры кнопки: цвет значка по умолчанию</span><span class="sxs-lookup"><span data-stu-id="47f66-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="47f66-130">Символьная строка</span><span class="sxs-lookup"><span data-stu-id="47f66-130">Character string</span></span> | <span data-ttu-id="47f66-131">Текстовое или шестнадцатеричное значение цвета символа кнопки.</span><span class="sxs-lookup"><span data-stu-id="47f66-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="47f66-132">Параметры кнопки: цвет значка "Активно"</span><span class="sxs-lookup"><span data-stu-id="47f66-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="47f66-133">Символьная строка</span><span class="sxs-lookup"><span data-stu-id="47f66-133">Character string</span></span> | <span data-ttu-id="47f66-134">Текстовое или шестнадцатеричное значение цвета выбранных символов кнопки.</span><span class="sxs-lookup"><span data-stu-id="47f66-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="47f66-135">Показать индекс</span><span class="sxs-lookup"><span data-stu-id="47f66-135">Show index</span></span> | <span data-ttu-id="47f66-136">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="47f66-136">**True** or **False**</span></span> | <span data-ttu-id="47f66-137">Если это свойство имеет значение **Истина**, то у каждого символа кнопки, который обозначает магазин, будет показан индекс.</span><span class="sxs-lookup"><span data-stu-id="47f66-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="47f66-138">Этот индекс будет соответствовать индексу в представлении списка, который отображается в модуле выбора магазина.</span><span class="sxs-lookup"><span data-stu-id="47f66-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="47f66-139">Добавление разрешенных URL-адресов для сопоставления в директивы политики безопасности содержимого сайта</span><span class="sxs-lookup"><span data-stu-id="47f66-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="47f66-140">Для взаимодействия модуля карты с Картами Bing необходимо убедиться, что следующие URL-адреса сопоставления разрешены в политике безопасности содержимого сайта (CSP).</span><span class="sxs-lookup"><span data-stu-id="47f66-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="47f66-141">Эта настройка выполняется в построителе сайтов Commerce путем добавления разрешенных URL-адресов в различные директивы CSP для сайта (например, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="47f66-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="47f66-142">Дополнительные сведения см. в разделе [Политика безопасности содержимого](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="47f66-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="47f66-143">В директиву **connect-src** добавьте **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="47f66-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="47f66-144">В директиву **img-src**, добавьте **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="47f66-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="47f66-145">В директиву **script-src** добавьте **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="47f66-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="47f66-146">В директиву **script style-src** добавьте **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="47f66-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="47f66-147">Добавление модуля карты на страницу</span><span class="sxs-lookup"><span data-stu-id="47f66-147">Add a map module to a page</span></span>

<span data-ttu-id="47f66-148">Подробные сведения о настройке модуля карты на странице см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="47f66-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="47f66-149">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="47f66-149">Additional resources</span></span>

[<span data-ttu-id="47f66-150">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="47f66-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="47f66-151">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="47f66-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="47f66-152">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="47f66-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="47f66-153">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="47f66-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="47f66-154">Управление картами Bing для вашей организации</span><span class="sxs-lookup"><span data-stu-id="47f66-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="47f66-155">Веб-элемент управления Карт Bing V8</span><span class="sxs-lookup"><span data-stu-id="47f66-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]