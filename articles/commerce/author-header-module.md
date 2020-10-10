---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 99457b2c98eae0ddd898f852630d690140a5a4c5
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817018"
---
# <a name="header-module"></a><span data-ttu-id="d3980-103">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="d3980-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d3980-104">В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3980-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3980-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d3980-105">Overview</span></span>

<span data-ttu-id="d3980-106">В Dynamics 365 Commerce заголовок страницы настраивается как фрагмент страницы, включающий заголовок, рекламный баннер и модули согласия на файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="d3980-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="d3980-107">Модуль заголовка включает логотип сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта, модуль значка корзины, список желаемого, параметры входа и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="d3980-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="d3980-108">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (другими словами, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="d3980-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="d3980-109">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="d3980-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="d3980-110">На следующем рисунке показан пример модуля заголовка на главной странице.</span><span class="sxs-lookup"><span data-stu-id="d3980-110">The following image shows an example of a header module on a home page.</span></span>

![Пример модуля заголовка](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="d3980-112">Свойства модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="d3980-112">Properties of a header module</span></span>

<span data-ttu-id="d3980-113">Модуль заголовка поддерживает свойства **Изображение логотипа**, **Ссылка на логотип** и **Ссылки на мою учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="d3980-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="d3980-114">Свойства **Изображение логотипа** и **Ссылка на логотип** используются для определения логотипа на странице.</span><span class="sxs-lookup"><span data-stu-id="d3980-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="d3980-115">Дополнительные сведения см. в разделе [Добавление логотипа](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="d3980-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="d3980-116">Свойство **Ссылки на мою учетную запись** можно использовать для определения страниц учетной записи, для которых владелец сайта хочет показывать быстрые ссылки в заголовке.</span><span class="sxs-lookup"><span data-stu-id="d3980-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="d3980-117">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="d3980-117">Modules that are available within a header module</span></span>

<span data-ttu-id="d3980-118">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="d3980-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="d3980-119">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="d3980-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="d3980-120">Дополнительные сведения см в разделе [Модуль меню навигации](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="d3980-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="d3980-121">**Поиск** — модуль поиска позволяет пользователям вводить искомые термины для поиска продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3980-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="d3980-122">URL-адрес страницы поиска по умолчанию и параметры запроса поиска должны быть указаны в **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="d3980-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="d3980-123">В модуле поиска есть свойства, позволяющие запретить кнопку поиска или метку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d3980-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="d3980-124">В модуле поиска также поддерживаются параметры автоматического предложения, такие как продукт, ключевое слово и результаты поиска категорий.</span><span class="sxs-lookup"><span data-stu-id="d3980-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="d3980-125">**Значок корзины** — модуль "значок корзины" представляет значок корзины, который отображает количество номенклатур в корзине в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="d3980-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="d3980-126">Дополнительные сведения см. в разделе [Модуль значка корзины](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="d3980-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="d3980-127">Создание фрагмента заголовка для страницы</span><span class="sxs-lookup"><span data-stu-id="d3980-127">Create a header fragment for a page</span></span>

<span data-ttu-id="d3980-128">Чтобы создать фрагмент заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d3980-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="d3980-129">Перейдите к разделу **Фрагменты**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="d3980-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d3980-130">В диалоговом окне **Создание фрагмента** выберите модуль **Контейнер**, введите имя для фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-131">Выберите ячейку **Контейнер по умолчанию**, а затем в области свойств справа задайте значение свойства **Ширина** как **Заполнить экран**.</span><span class="sxs-lookup"><span data-stu-id="d3980-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="d3980-132">В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="d3980-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3980-133">В диалоговом окне **Добавление модуля** выберите модули **Согласие на файлы cookie**, **Заголовок** и **Рекламный баннер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-134">В области свойства модуля **Рекламный баннер** выберите **Добавить сообщение**, затем выберите **Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="d3980-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="d3980-135">В диалоговом окне **Сообщение** добавьте текст и ссылки для рекламного содержимого, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-136">В области свойств модуля **Согласие на файлы cookie** добавьте и настройте текст и ссылку на страницу конфиденциальности сайта.</span><span class="sxs-lookup"><span data-stu-id="d3980-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="d3980-137">В ячейке **Меню навигации** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="d3980-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3980-138">В диалоговом окне **Добавить модуль** выберите модуль **Меню навигации**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-139">В области свойств модуля меню навигация в области **Источник для меню навигации** выберите **Retail Server**.</span><span class="sxs-lookup"><span data-stu-id="d3980-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="d3980-140">В области свойств модуля меню навигации в разделе **Статические пункты меню** выберите **Добавить пункт меню**, затем выберите **Пункт меню**.</span><span class="sxs-lookup"><span data-stu-id="d3980-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="d3980-141">В диалоговом окне **Пункт меню** в поле **Текст пункта меню** введите "Контакты".</span><span class="sxs-lookup"><span data-stu-id="d3980-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="d3980-142">В диалоговом окне **Пункт меню** в поле **Цель ссылки пункта меню** выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="d3980-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="d3980-143">В диалоговом окне **Добавление ссылки** выберите URL-адрес страницы "Контакты" сайта, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="d3980-144">В диалоговом окне **Пункт меню** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="d3980-145">В ячейке **Поиск** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="d3980-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3980-146">В диалоговом окне **Добавить модуль** выберите модуль **Поиск**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-147">В области свойств модуля поиска настройте свойства.</span><span class="sxs-lookup"><span data-stu-id="d3980-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="d3980-148">В ячейке **Значок корзины** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="d3980-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3980-149">В диалоговом окне **Добавить модуль** выберите модуль **Значок корзины**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d3980-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3980-150">В области свойств модуля значка корзины настройте свойства.</span><span class="sxs-lookup"><span data-stu-id="d3980-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="d3980-151">Если необходимо, чтобы значок корзины отображал сводку корзины (также называемую мини-корзиной), когда пользователь наводит на него указатель мыши, установите флажок **Показывать мини-корзину**.</span><span class="sxs-lookup"><span data-stu-id="d3980-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="d3980-152">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="d3980-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="d3980-153">Чтобы обеспечить, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="d3980-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="d3980-154">В слоте **Заголовок** модуля **Страница по умолчанию** добавьте созданный фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="d3980-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="d3980-155">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="d3980-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3980-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3980-156">Additional resources</span></span>

[<span data-ttu-id="d3980-157">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="d3980-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d3980-158">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="d3980-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d3980-159">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="d3980-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d3980-160">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="d3980-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d3980-161">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="d3980-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="d3980-162">Согласие на файлы cookie</span><span class="sxs-lookup"><span data-stu-id="d3980-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="d3980-163">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="d3980-163">Footer module</span></span>](author-footer-module.md)
