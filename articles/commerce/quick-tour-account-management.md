---
title: Обзор страниц управления учетной записью
description: В этом разделе представлен обзор страниц управления учетными записями в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d0e066428e8c4717b5a50144f63e59b87089d286
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415346"
---
# <a name="account-management-pages-overview"></a><span data-ttu-id="04553-103">Обзор страниц управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="04553-103">Account management pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04553-104">В этом разделе представлен обзор страниц управления учетными записями в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="04553-104">This topic provides an overview of account management pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="04553-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="04553-105">Overview</span></span>

<span data-ttu-id="04553-106">Страницы управления учетными записями позволяют клиентам просматривать сведения, имеющие отношение к их учетным записям и заказам.</span><span class="sxs-lookup"><span data-stu-id="04553-106">Account management pages let customers view information that is related to their account and orders.</span></span> <span data-ttu-id="04553-107">Страницы управления учетными записями включают целевую страницу управления учетными записями и страницы для профиля пользователя, адресов, журнала заказов, сведений о заказе, баллов по программы лояльности и списка желаний.</span><span class="sxs-lookup"><span data-stu-id="04553-107">Account management pages include the account management landing page, and pages for the user's profile, addresses, order history, order details, loyalty points, and wish list.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="04553-108">Целевая страница управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="04553-108">Account management landing page</span></span>

<span data-ttu-id="04553-109">Когда клиент выполняет вход и выбирает пункт **Моя учетная запись**, открывается целевая страница управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="04553-109">When a customer signs in and selects **My Account**, the account management landing page is opened.</span></span> <span data-ttu-id="04553-110">На этой странице содержится краткая сводка по всем сведениям, относящимися к данной учетной записи, такие как профиль пользователя, заказы, список желаний, адреса, баллы по программе лояльности.</span><span class="sxs-lookup"><span data-stu-id="04553-110">This page provides a quick summary of all account-related information, such as the user's profile, orders, wish list, addresses, loyalty points.</span></span> <span data-ttu-id="04553-111">С этой страницы у клиента может быть доступ к дополнительным сведениям для каждой области.</span><span class="sxs-lookup"><span data-stu-id="04553-111">From this page, the customer can access more details for each area.</span></span>

<span data-ttu-id="04553-112">На следующем рисунке показан пример целевой страницы управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="04553-112">The following illustration shows an example of the account management landing page.</span></span>

![Пример целевой страницы управления учетной записью](./media/Account-Management.PNG)

### <a name="my-profile-page"></a><span data-ttu-id="04553-114">Страница "Мой профиль"</span><span class="sxs-lookup"><span data-stu-id="04553-114">My profile page</span></span>

<span data-ttu-id="04553-115">На странице **Мой профиль** отображаются сведения об учетной записи клиента, такие как имя и номер телефона.</span><span class="sxs-lookup"><span data-stu-id="04553-115">The **My profile** page shows customer's account information, such as his or her name and phone number.</span></span> <span data-ttu-id="04553-116">Клиент может обновить сведения о своем профиле на этой странице.</span><span class="sxs-lookup"><span data-stu-id="04553-116">The customer can update his or her profile information on this page.</span></span> <span data-ttu-id="04553-117">Эту страницу можно настроить таким образом, чтобы она включала дополнительные настройки учетной записи клиента, такие как параметр для согласия на получение маркетинговых сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="04553-117">This page can be customized so that it includes additional customer account preferences, such as an option for opting in to marketing email.</span></span>

<span data-ttu-id="04553-118">На следующем рисунке показан пример страницы **Мой профиль**, которая была создана с помощью библиотеки модулей.</span><span class="sxs-lookup"><span data-stu-id="04553-118">The following illustration shows an example of a **My profile** page that was built by using the module library.</span></span>

![Пример страницы "Мой профиль"](./media/Account-Management-MyProfile.PNG)

### <a name="addresses-page"></a><span data-ttu-id="04553-120">Страница адресов</span><span class="sxs-lookup"><span data-stu-id="04553-120">Addresses page</span></span>

<span data-ttu-id="04553-121">Страница **Адреса** позволяет клиенту добавлять адреса в свою учетную запись.</span><span class="sxs-lookup"><span data-stu-id="04553-121">The **Addresses** page lets the customer add addresses to his or her account.</span></span> <span data-ttu-id="04553-122">Здесь также отображается список адресов, которые клиент ранее добавил или сохранил в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04553-122">It also shows the list of addresses that the customer has previously added or saved to the account.</span></span> <span data-ttu-id="04553-123">Эти адреса являются адресами, введенными клиентом либо на данной странице, либо при размещении заказа.</span><span class="sxs-lookup"><span data-stu-id="04553-123">These addresses are addresses that the customer entered either on this page or while placing an order.</span></span>

<span data-ttu-id="04553-124">На следующем рисунке показан пример страницы **Адреса**.</span><span class="sxs-lookup"><span data-stu-id="04553-124">The following illustration shows an example of the **Addresses** page.</span></span>

![Пример страницы адресов](./media/Account-Management-Address.png)

### <a name="order-history-and-order-details-pages"></a><span data-ttu-id="04553-126">Страницы истории заказов и сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="04553-126">Order history and Order details pages</span></span>

<span data-ttu-id="04553-127">На странице **История заказов** отображается сводка по всем заказам, отправленным клиентом с помощью своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04553-127">The **Order history** page shows a summary of all orders that the customer has submitted by using his or her account.</span></span> <span data-ttu-id="04553-128">Она предоставляет быструю сводку по заказанным номенклатурам, номер подтверждения, код продажи, сведения для отслеживания и другую информацию.</span><span class="sxs-lookup"><span data-stu-id="04553-128">It gives a quick summary of the items that were ordered, the confirmation number, sales ID, tracking information, and other information.</span></span> <span data-ttu-id="04553-129">Если клиент хочет просмотреть более детализированную разбивку для каждого заказа, имеется страница **Сведения о заказе**.</span><span class="sxs-lookup"><span data-stu-id="04553-129">If the customer wants to view a more detailed breakdown of each order, there is an **Order details** page.</span></span> <span data-ttu-id="04553-130">Эта страница включает такие сведения, как адрес доставки, сведения о платежах, скидки, налоги и затраты на доставку по данному заказу.</span><span class="sxs-lookup"><span data-stu-id="04553-130">This page includes information such as the shipping address, payment information, discounts, taxes, and shipping costs for the order.</span></span>

<span data-ttu-id="04553-131">На следующем рисунке показан пример страницы **История заказов**.</span><span class="sxs-lookup"><span data-stu-id="04553-131">The following illustration shows an example of the **Order history** page.</span></span>

![Пример страницы истории заказов](./media/Account-Management-OrderHistory.PNG)

<span data-ttu-id="04553-133">На следующем рисунке показан пример страницы **Сведения о заказе**.</span><span class="sxs-lookup"><span data-stu-id="04553-133">The following illustration shows an example of the **Order details** page.</span></span>

![Пример страницы сведений о заказе](./media/Account-Management-OrderDetails.PNG)

### <a name="loyalty-program-page"></a><span data-ttu-id="04553-135">Страница программы лояльности</span><span class="sxs-lookup"><span data-stu-id="04553-135">Loyalty program page</span></span>

<span data-ttu-id="04553-136">Страница **Программа лояльности** позволяет клиенту стать членом программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="04553-136">The **Loyalty program** page lets the customer become a member of a loyalty program.</span></span> <span data-ttu-id="04553-137">После регистрации клиента в программе лояльности страница **Программа лояльности** включает такие сведения, как количество заработанных баллов и число баллов, которые были погашены.</span><span class="sxs-lookup"><span data-stu-id="04553-137">After a customer has signed up for a loyalty program, the **Loyalty program** page include details such as the number of points that have been earned and the number of points that have been redeemed.</span></span>

<span data-ttu-id="04553-138">Следующая иллюстрация показывает пример страницы **Программа лояльности**.</span><span class="sxs-lookup"><span data-stu-id="04553-138">The following illustration shows an example of a **Loyalty program** page.</span></span>

![Пример страницы программы лояльности](./media/Account-Management-Loyalty.PNG)

### <a name="wishlist-page"></a><span data-ttu-id="04553-140">Страница списка пожеланий</span><span class="sxs-lookup"><span data-stu-id="04553-140">Wishlist page</span></span>

<span data-ttu-id="04553-141">Страница **Список желаний** содержит список номенклатур, добавленных клиентом в свой список желаний.</span><span class="sxs-lookup"><span data-stu-id="04553-141">The **Wishlist** page shows a list of the items that the customer has added to his or her wish list.</span></span> <span data-ttu-id="04553-142">В список желаний можно добавить продукты и варианты продуктов.</span><span class="sxs-lookup"><span data-stu-id="04553-142">Both products and product variants can be added to the wish list.</span></span> <span data-ttu-id="04553-143">С этой страницы клиент может удалить номенклатуру из списка желаний или добавить номенклатуру непосредственно в корзину.</span><span class="sxs-lookup"><span data-stu-id="04553-143">From this page, the customer can remove an item from the wish list or add an item directly to the cart.</span></span>

<span data-ttu-id="04553-144">Следующая иллюстрация показывает пример страницы **Список желаний**.</span><span class="sxs-lookup"><span data-stu-id="04553-144">The following illustration shows an example of a **Wishlist** page.</span></span>

![Пример страницы списка желаний](./media/Account-Management-Wishlist.PNG)

<span data-ttu-id="04553-146">Дополнительные сведения о модулях управления учетными записями и способах их создания см. в разделе [Управление учетными записями](account-management.md).</span><span class="sxs-lookup"><span data-stu-id="04553-146">For more information about account management modules and how to author them, see [Account Management](account-management.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04553-147">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04553-147">Additional resources</span></span>

[<span data-ttu-id="04553-148">Обзор домашней страницы</span><span class="sxs-lookup"><span data-stu-id="04553-148">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="04553-149">Обзор страниц сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="04553-149">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="04553-150">Обзор страниц корзины и оформления заказа</span><span class="sxs-lookup"><span data-stu-id="04553-150">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

