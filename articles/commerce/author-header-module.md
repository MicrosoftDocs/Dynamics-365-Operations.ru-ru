---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025696"
---
# <a name="header-module"></a><span data-ttu-id="a136e-103">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="a136e-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a136e-104">В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a136e-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a136e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="a136e-105">Overview</span></span>

<span data-ttu-id="a136e-106">В Dynamics 365 Commerce заголовок страницы состоит из нескольких модулей, таких как заголовок, меню переходов, поиск, рекламный баннер и согласие на файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="a136e-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="a136e-107">Модуль заголовка включает логотип сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта, символ корзины, список желаемого, параметры входа и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="a136e-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="a136e-108">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (другими словами, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="a136e-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="a136e-109">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="a136e-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="a136e-110">Свойства модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="a136e-110">Properties of a header module</span></span>

<span data-ttu-id="a136e-111">Модуль заголовка поддерживает свойства **Изображение логотипа**, **Ссылка на логотип** и **Ссылки на мою учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="a136e-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="a136e-112">Свойства **Изображение логотипа** и **Ссылка на логотип** используются для определения логотипа на странице.</span><span class="sxs-lookup"><span data-stu-id="a136e-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="a136e-113">Дополнительные сведения см. в разделе [Добавление логотипа](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="a136e-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="a136e-114">Свойство **Ссылки на мою учетную запись** можно использовать для определения страниц учетной записи, для которых владелец сайта хочет показывать быстрые ссылки в заголовке.</span><span class="sxs-lookup"><span data-stu-id="a136e-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="a136e-115">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="a136e-115">Modules that are available in a header module</span></span>

<span data-ttu-id="a136e-116">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="a136e-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="a136e-117">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="a136e-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="a136e-118">Иерархия навигации по каналу может быть настроена в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a136e-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a136e-119">В меню навигации есть свойство **Источник навигации**, которое используется для указания пунктов меню навигации Retail Server и статических пунктов меню в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="a136e-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="a136e-120">Если в качестве источника указан статический пункт меню, могут быть предоставлены относительные ссылки на другие страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="a136e-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="a136e-121">Сконфигурированные элементы затем отображаются в виде навигации заголовка.</span><span class="sxs-lookup"><span data-stu-id="a136e-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="a136e-122">**Поиск** — модуль поиска позволяет пользователям вводить искомые термины для поиска продуктов.</span><span class="sxs-lookup"><span data-stu-id="a136e-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="a136e-123">URL-адрес страницы поиска по умолчанию и параметры запроса поиска должны быть указаны в **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="a136e-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="a136e-124">В модуле поиска есть свойства, позволяющие запретить кнопку поиска или метку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a136e-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="a136e-125">В модуле поиска также поддерживаются параметры автоматического предложения, такие как продукт, ключевое слово и результаты поиска категорий.</span><span class="sxs-lookup"><span data-stu-id="a136e-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="a136e-126">Создание модуля заголовка для страницы</span><span class="sxs-lookup"><span data-stu-id="a136e-126">Create a header module for a page</span></span>

<span data-ttu-id="a136e-127">Чтобы создать модуль заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a136e-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="a136e-128">Создайте фрагмент с именем **Фрагмент заголовка** и добавьте в него модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="a136e-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="a136e-129">В области свойств модуля контейнера задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="a136e-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="a136e-130">Добавление модулей рекламного баннера и согласия на файлы cookie в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="a136e-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="a136e-131">Добавьте еще один модуль контейнера во фрагмент и задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="a136e-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="a136e-132">Добавьте модуль заголовка во второй модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="a136e-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="a136e-133">В области **Меню навигация** модуля заголовка добавьте модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="a136e-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="a136e-134">В области свойств модуля меню переходов настройте свойства модуля меню навигации.</span><span class="sxs-lookup"><span data-stu-id="a136e-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="a136e-135">В области **Поиск** модуля заголовка добавьте модуль поиска.</span><span class="sxs-lookup"><span data-stu-id="a136e-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="a136e-136">В области свойств модуля поиска настройте свойства модуля поиска.</span><span class="sxs-lookup"><span data-stu-id="a136e-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="a136e-137">Сохраните фрагмент страницы, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="a136e-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="a136e-138">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="a136e-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="a136e-139">В области **Основной** на странице по умолчанию добавьте фрагмент страницы заголовка, содержащий модуль заголовка, к заголовку.</span><span class="sxs-lookup"><span data-stu-id="a136e-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="a136e-140">Сохраните шаблон, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="a136e-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a136e-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a136e-141">Additional resources</span></span>

[<span data-ttu-id="a136e-142">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="a136e-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a136e-143">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="a136e-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a136e-144">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="a136e-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a136e-145">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="a136e-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a136e-146">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="a136e-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a136e-147">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="a136e-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a136e-148">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="a136e-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a136e-149">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="a136e-149">Footer module</span></span>](author-footer-module.md)
