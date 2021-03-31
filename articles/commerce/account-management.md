---
title: Страницы и модули управления учетной записью
description: В этом разделе рассматриваются страницы и модули управления учетными записями в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206639"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="dfa3d-103">Страницы и модули управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="dfa3d-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dfa3d-104">В этом разделе рассматриваются страницы и модули управления учетными записями в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dfa3d-105">Управление учетными записями относится к группе страниц, используемых для управления информацией, относящейся к учетным записям пользователей в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="dfa3d-106">Страницы управления учетными записями включают целевую страницу управления учетными записями, страницу профиля пользователя, страницу адрес пользователя, страницу журнал заказов, страницу сведений о заказе, страницу программы лояльности и страницу списка желаний.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="dfa3d-107">Целевая страница управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="dfa3d-107">Account management landing page</span></span>

<span data-ttu-id="dfa3d-108">Целевая страница управления учетными записями использует следующие модули:</span><span class="sxs-lookup"><span data-stu-id="dfa3d-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="dfa3d-109">**Контейнер** — все модули целевых страниц управления учетными записями должны размещаться в контейнере.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="dfa3d-110">**Плитка приветствия для учетной записи** — этот модуль используется для предоставления приветственного сообщения на странице управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="dfa3d-111">Он включает в себя свойства заголовка.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="dfa3d-112">**Универсальная плитка для учетной записи** — этот модуль может использоваться для представления заголовков и ссылок на страницы управления учетными записями, например на страницах "История заказов" или "Мой профиль".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="dfa3d-113">Модуль универсальной плитки может использоваться для настройки плитки для любой страницы.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="dfa3d-114">В Fabrikam этот модуль используется для ссылок на страницы "История заказов" и "Мой профиль" на начальной странице управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="dfa3d-115">**Плитка списка желаний учетной записи** — этот модуль используется для предоставления сводки по номенклатурам из списка желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="dfa3d-116">Например, это может быть сообщение: "У вас 10 товаров в списке желаний".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="dfa3d-117">Он включает в себя свойства для заголовка и ссылки "Просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="dfa3d-118">Ссылку "Просмотр сведений" следует настроить для перенаправления на страницу списка желаний.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="dfa3d-119">**Плитка адреса учетной записи** — этот модуль используется для предоставления сводки об адресах пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="dfa3d-120">Например, это может быть сообщение: "К вашей учетной записи добавлены два адреса".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="dfa3d-121">Он включает в себя свойства для заголовка и ссылки "Просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="dfa3d-122">Ссылку "Просмотр сведений" следует настроить для перенаправления на страницу адреса пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="dfa3d-123">**Плитка программы лояльности для учетной записи** — этот модуль используется для отображения сведений о программе лояльности и связывания с ней.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="dfa3d-124">Эта плитка имеет два состояния: в одном состоянии отображаются ссылки для присоединения к программе лояльности, если пользователь еще не является участником группы.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="dfa3d-125">В другом состоянии отображаются ссылки для просмотра страницы сведений о программе лояльности, когда пользователь уже является участником группы.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="dfa3d-126">Свойства включают заголовок, ссылку "Регистрация", а также ссылку "Просмотр программы лояльности".</span><span class="sxs-lookup"><span data-stu-id="dfa3d-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="dfa3d-127">Ссылку "Просмотр программы лояльности" следует настроить для перенаправления на страницу программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="dfa3d-128">Ссылка "Регистрация" должна быть настроена для перенаправления на страницу, на которой пользователи могут присоединиться к программе лояльности.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="dfa3d-129">Страница журнала заказов</span><span class="sxs-lookup"><span data-stu-id="dfa3d-129">Order history page</span></span>

<span data-ttu-id="dfa3d-130">Страница журнала заказов использует модуль истории заказов для отображения всех последних заказов, размещенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="dfa3d-131">Страница сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="dfa3d-131">Order details page</span></span>

<span data-ttu-id="dfa3d-132">Страница сведений о заказе содержит подробную информацию по каждому заказу и доступна со страницы журнала заказов.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="dfa3d-133">Она использует модуль сведений о заказе, которому для получения сведений о заказе требуется идентификатор продаж или код проводки.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="dfa3d-134">Страница профиля пользователя</span><span class="sxs-lookup"><span data-stu-id="dfa3d-134">User profile page</span></span>

<span data-ttu-id="dfa3d-135">На странице профиля пользователя отображаются сведения об учетной записи пользователя, такие как имя пользователя и адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="dfa3d-136">Он использует сведения о профиле пользователя и модули редактирования профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="dfa3d-137">Хотя адрес электронной почты не может быть удален, его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="dfa3d-138">Страница профиля пользователя также показывает предпочтения пользователей, которые позволяют пользователю отказаться от определенных функций, таких как персонализация списков рекомендаций, или включить их.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="dfa3d-139">Страница адреса пользователя</span><span class="sxs-lookup"><span data-stu-id="dfa3d-139">User address page</span></span>

<span data-ttu-id="dfa3d-140">Страница адреса пользователя показывает список адресов, связанных с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="dfa3d-141">Пользователь предоставил эти адреса во время оформления заказа или добавил их непосредственно на этой странице.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="dfa3d-142">Модуль адреса пользователя используется для добавления и изменения адресов, установки основного адреса и отображения существующих адресов на странице.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="dfa3d-143">Страница списка желаний</span><span class="sxs-lookup"><span data-stu-id="dfa3d-143">Wish list page</span></span>

<span data-ttu-id="dfa3d-144">На странице списка желаний отображаются номенклатуры, добавленные в список желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="dfa3d-145">Она использует модуль списка желаний для отображения номенклатур списка желаний.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="dfa3d-146">Страница лояльности</span><span class="sxs-lookup"><span data-stu-id="dfa3d-146">Loyalty page</span></span>

<span data-ttu-id="dfa3d-147">Страница программы лояльности позволяет клиентам просмотреть сведения о программе лояльности, если они уже являются участниками программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="dfa3d-148">Они также могут просматривать заработанные и погашенные баллы в последних проводках.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="dfa3d-149">Страница использует модуль сведений о программе лояльности для показа сведений о программе лояльности.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="dfa3d-150">Чтобы присоединиться к программе лояльности, можно создать маркетинговую страницу с помощью модуля регистрации в программе лояльности и модуля условии программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="dfa3d-151">Если пользователь не является участником программы лояльности, эти модули позволят пользователю зарегистрироваться.</span><span class="sxs-lookup"><span data-stu-id="dfa3d-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfa3d-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dfa3d-152">Additional resources</span></span>

[<span data-ttu-id="dfa3d-153">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="dfa3d-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="dfa3d-154">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="dfa3d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="dfa3d-155">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="dfa3d-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="dfa3d-156">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="dfa3d-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="dfa3d-157">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="dfa3d-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="dfa3d-158">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="dfa3d-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="dfa3d-159">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="dfa3d-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="dfa3d-160">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="dfa3d-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]