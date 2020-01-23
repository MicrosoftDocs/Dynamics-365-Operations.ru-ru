---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885486"
---
# <a name="header-module"></a><span data-ttu-id="51a71-103">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="51a71-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="51a71-104">В этом разделе описываются модули заголовка, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51a71-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="51a71-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="51a71-105">Overview</span></span>

<span data-ttu-id="51a71-106">Модуль заголовка — это специальный контейнер, который используется для размещения всех модулей, которые будут отображаться в заголовке страницы.</span><span class="sxs-lookup"><span data-stu-id="51a71-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="51a71-107">Например, он может содержать эмблему сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="51a71-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="51a71-108">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (то есть, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="51a71-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="51a71-109">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="51a71-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="51a71-110">Свойства заголовка</span><span class="sxs-lookup"><span data-stu-id="51a71-110">Properties of a header</span></span>

<span data-ttu-id="51a71-111">Как и в случае универсальных контейнеров, модуль заголовка поддерживает свойства **заголовок** и **ширина**.</span><span class="sxs-lookup"><span data-stu-id="51a71-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="51a71-112">В модуле заголовка имеется несколько слотов.</span><span class="sxs-lookup"><span data-stu-id="51a71-112">A header module has multiple slots.</span></span> <span data-ttu-id="51a71-113">Например, существуют гнезда для информационного сообщения, меню навигации, эмблемы, панели поиска, значка корзины, значка списка желаний и информации об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="51a71-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="51a71-114">Каждый слот поддерживает конкретный набор модулей.</span><span class="sxs-lookup"><span data-stu-id="51a71-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="51a71-115">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="51a71-115">Modules that are available in a header module</span></span>

<span data-ttu-id="51a71-116">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="51a71-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="51a71-117">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="51a71-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="51a71-118">Иерархия навигации по каналу может быть настроена в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="51a71-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="51a71-119">Сконфигурированные элементы затем отображаются в виде навигации заголовка.</span><span class="sxs-lookup"><span data-stu-id="51a71-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="51a71-120">Кроме того, можно настроить статические ссылки навигации, а также указать относительные ссылки на другие страницы сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="51a71-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="51a71-121">Сам заголовок может быть выровнен по левому краю, по правому или по центру.</span><span class="sxs-lookup"><span data-stu-id="51a71-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="51a71-122">**Значок корзины** — значок корзины представляет собой специальный значок, представляющий корзину.</span><span class="sxs-lookup"><span data-stu-id="51a71-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="51a71-123">Он отображается в заголовке и указывает количество номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="51a71-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="51a71-124">Ссылка на страницу корзины должна сопровождаться значком корзины, чтобы клиенты могли быть перенаправлены на страницу корзины при взаимодействии со значком.</span><span class="sxs-lookup"><span data-stu-id="51a71-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="51a71-125">**Значок списка желаний** — значок списка желаемых товаров отображается в заголовке и указывает число номенклатур, добавленных в список желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="51a71-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="51a71-126">Ссылка на страницу списка желаний должна сопровождаться этим значком, чтобы клиенты могли быть перенаправлены на страницу списка желаний при взаимодействии со значком.</span><span class="sxs-lookup"><span data-stu-id="51a71-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="51a71-127">**Модуль входа** — в заголовке отображается модуль входа в систему.</span><span class="sxs-lookup"><span data-stu-id="51a71-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="51a71-128">Клиенты могут либо войти в учетную запись, либо зарегистрировать учетную запись.</span><span class="sxs-lookup"><span data-stu-id="51a71-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="51a71-129">Если клиент уже выполнил вход, модуль можно настроить так, чтобы он отображал ссылки на страницу учетной записи, страницу журнала заказов или другую страницу.</span><span class="sxs-lookup"><span data-stu-id="51a71-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="51a71-130">**Модуль эмблемы** — в этом модуле отображается эмблема, представляющая розничного продавца и торговую марку.</span><span class="sxs-lookup"><span data-stu-id="51a71-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="51a71-131">Это изображение, имеющее ссылку.</span><span class="sxs-lookup"><span data-stu-id="51a71-131">It's an image that has a link.</span></span> <span data-ttu-id="51a71-132">Ссылка обычно настраивается таким образом, чтобы она перенаправлялась на домашнюю страницу. Поэтому клиенты могут быстро вернуться на домашнюю страницу с любой страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="51a71-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="51a71-133">**Оповещение** — оповещение отображается в заголовке и используется для отображения встроенного сообщения, которое применяется ко всем страницам сайта.</span><span class="sxs-lookup"><span data-stu-id="51a71-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="51a71-134">Например, оповещение может содержать сообщение "Ежегодная распродажа заканчивается через 2 дня".</span><span class="sxs-lookup"><span data-stu-id="51a71-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="51a71-135">**Панель поиска** — панель поиска позволяет пользователям вводить искомые термины, чтобы они могли выполнять поиск продуктов.</span><span class="sxs-lookup"><span data-stu-id="51a71-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="51a71-136">Модуль должен быть настроен с URL-адресом страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="51a71-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="51a71-137">Можно настроить параметр строки запроса (значение по умолчанию — **"q"**).</span><span class="sxs-lookup"><span data-stu-id="51a71-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="51a71-138">Панель поиска содержит ячейку автоматического предложения, в которую следует добавить модуль автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="51a71-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="51a71-139">**Автозаполнение** — автоматически предлагаемые результаты отображаются в модуле автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="51a71-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="51a71-140">Эти результаты могут быть ключевыми словами, продуктами или категориями, в которых искомый термин будет найден.</span><span class="sxs-lookup"><span data-stu-id="51a71-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="51a71-141">Создание модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="51a71-141">Create a header module</span></span>

<span data-ttu-id="51a71-142">Чтобы создать модуль заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="51a71-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="51a71-143">Создайте фрагмент страницы, содержащий модуль заголовка.</span><span class="sxs-lookup"><span data-stu-id="51a71-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="51a71-144">Добавьте модули в гнезда в модуле заголовка.</span><span class="sxs-lookup"><span data-stu-id="51a71-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="51a71-145">Обновите настройки для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="51a71-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="51a71-146">Сохраните фрагмент страницы.</span><span class="sxs-lookup"><span data-stu-id="51a71-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="51a71-147">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="51a71-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="51a71-148">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="51a71-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="51a71-149">На странице по умолчанию добавьте фрагмент страницы, содержащий модуль заголовка, к заголовку в главном слоте.</span><span class="sxs-lookup"><span data-stu-id="51a71-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="51a71-150">Сохраните шаблон.</span><span class="sxs-lookup"><span data-stu-id="51a71-150">Save the template.</span></span> 
1. <span data-ttu-id="51a71-151">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="51a71-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51a71-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51a71-152">Additional resources</span></span>

[<span data-ttu-id="51a71-153">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="51a71-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="51a71-154">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="51a71-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="51a71-155">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="51a71-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="51a71-156">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="51a71-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="51a71-157">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="51a71-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="51a71-158">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="51a71-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="51a71-159">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="51a71-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="51a71-160">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="51a71-160">Footer module</span></span>](author-footer-module.md)
