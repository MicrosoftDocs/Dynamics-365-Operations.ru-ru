---
title: Страницы и модули управления учетными записями
description: В этом разделе рассматриваются страницы и модули управления учетными записями в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885817"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="21df7-103">Страницы и модули управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="21df7-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="21df7-104">В этом разделе рассматриваются страницы и модули управления учетными записями в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21df7-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="21df7-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="21df7-105">Overview</span></span>

<span data-ttu-id="21df7-106">Управление учетными записями относится к группе страниц, используемых для управления информацией, относящейся к учетным записям пользователей в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21df7-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="21df7-107">Страницы управления учетными записями включают целевую страницу управления учетными записями, страницу профиля пользователя, страницу адрес пользователя, страницу журнал заказов, страницу сведений о заказе, страницу программы лояльности и страницу списка желаний.</span><span class="sxs-lookup"><span data-stu-id="21df7-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="21df7-108">Целевая страница управления учетной записью</span><span class="sxs-lookup"><span data-stu-id="21df7-108">Account management landing page</span></span>

<span data-ttu-id="21df7-109">Целевая страница управления учетными записями использует следующие модули:</span><span class="sxs-lookup"><span data-stu-id="21df7-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="21df7-110">**Размещение содержимого** — этот модуль является контейнерным модулем, хранящим все модули на целевой странице управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="21df7-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="21df7-111">**Элемент приветствия для учетной записи** — этот модуль используется для предоставления приветственного сообщения на странице управления учетными записями.</span><span class="sxs-lookup"><span data-stu-id="21df7-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="21df7-112">Он включает в себя свойства для заголовка и размера плитки.</span><span class="sxs-lookup"><span data-stu-id="21df7-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="21df7-113">Свойство **Размер плитки** определяет ширину модуля в модуле размещения содержимого.</span><span class="sxs-lookup"><span data-stu-id="21df7-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="21df7-114">Диапазон значений от **1** до **12**, где **12** обозначает полную ширину контейнера размещения содержимого.</span><span class="sxs-lookup"><span data-stu-id="21df7-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="21df7-115">**Элемент размещения заказов по учетной записи** — этот модуль используется для размещения сводки по количеству заказов, размещенных по учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="21df7-116">Он включает в себя свойства для заголовка, размера плитки и ссылки "просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="21df7-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="21df7-117">Ссылку "просмотр сведений" следует настроить для перенаправления на страницу журнала заказов.</span><span class="sxs-lookup"><span data-stu-id="21df7-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="21df7-118">**Элемент размещения профиля учетной записи** — этот модуль используется для предоставления сводки о профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="21df7-119">Он включает в себя свойства для заголовка, размера плитки и ссылки "просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="21df7-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="21df7-120">Ссылку "просмотр сведений" следует настроить для перенаправления на страницу профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="21df7-121">**Элемент списка желаний учетной записи** — этот модуль используется для предоставления сводки по номенклатурам из списка желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="21df7-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="21df7-122">Например, это может быть сообщение: "У вас 10 товаров в списке желаний".</span><span class="sxs-lookup"><span data-stu-id="21df7-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="21df7-123">Он включает в себя свойства для заголовка, размера плитки и ссылки "просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="21df7-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="21df7-124">Ссылку "просмотр сведений" следует настроить для перенаправления на страницу списка желаний.</span><span class="sxs-lookup"><span data-stu-id="21df7-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="21df7-125">**Элемент адреса учетной записи** — этот модуль используется для предоставления сводки об адресах пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="21df7-126">Например, это может быть сообщение: "К вашей учетной записи добавлены два адреса".</span><span class="sxs-lookup"><span data-stu-id="21df7-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="21df7-127">Он включает в себя свойства для заголовка, размера плитки и ссылки "просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="21df7-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="21df7-128">Ссылку "просмотр сведений" следует настроить для перенаправления на страницу адреса пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="21df7-129">**Элемент программы лояльности для учетной записи** — этот модуль используется для отображения сведений о программе лояльности и связывания с ней.</span><span class="sxs-lookup"><span data-stu-id="21df7-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="21df7-130">Он включает в себя свойства для заголовка, размера плитки и ссылки "просмотр сведений", а также ссылку "стать участником".</span><span class="sxs-lookup"><span data-stu-id="21df7-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="21df7-131">Ссылку "просмотр сведений" следует настроить для перенаправления на страницу программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="21df7-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="21df7-132">Ссылка "стать участником" должна быть настроена для перенаправления на страницу, на которой пользователи могут присоединиться к программе лояльности.</span><span class="sxs-lookup"><span data-stu-id="21df7-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="21df7-133">Страница журнала заказов</span><span class="sxs-lookup"><span data-stu-id="21df7-133">Order history page</span></span>

<span data-ttu-id="21df7-134">Страница журнала заказов использует модуль истории заказов для отображения всех последних заказов, размещенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="21df7-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="21df7-135">Страница сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="21df7-135">Order details page</span></span>

<span data-ttu-id="21df7-136">Страница сведений о заказе содержит подробную информацию по каждому заказу и доступна со страницы журнала заказов.</span><span class="sxs-lookup"><span data-stu-id="21df7-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="21df7-137">Она использует модуль сведений о заказе, которому для получения сведений о заказе требуется идентификатор продаж или код проводки.</span><span class="sxs-lookup"><span data-stu-id="21df7-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="21df7-138">Страница профиля пользователя</span><span class="sxs-lookup"><span data-stu-id="21df7-138">User profile page</span></span>

<span data-ttu-id="21df7-139">На странице профиля пользователя отображаются сведения об учетной записи пользователя, такие как имя пользователя и адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="21df7-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="21df7-140">На ней нем используется модуль профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="21df7-140">It uses the user profile module.</span></span> <span data-ttu-id="21df7-141">Хотя адрес электронной почты не может быть удален, его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="21df7-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="21df7-142">Страница профиля пользователя также показывает предпочтения пользователей, которые позволяют пользователю отказаться от определенных функций, таких как персонализация списков рекомендаций, или включить их.</span><span class="sxs-lookup"><span data-stu-id="21df7-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="21df7-143">Страница адреса пользователя</span><span class="sxs-lookup"><span data-stu-id="21df7-143">User address page</span></span>

<span data-ttu-id="21df7-144">Страница адреса пользователя показывает список адресов, связанных с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="21df7-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="21df7-145">Пользователь предоставил эти адреса во время оформления заказа или добавил их непосредственно на этой странице.</span><span class="sxs-lookup"><span data-stu-id="21df7-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="21df7-146">Модуль адреса пользователя используется для добавления и изменения адресов, установки основного адреса и отображения существующих адресов на странице.</span><span class="sxs-lookup"><span data-stu-id="21df7-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="21df7-147">Страница списка желаний</span><span class="sxs-lookup"><span data-stu-id="21df7-147">Wish list page</span></span>

<span data-ttu-id="21df7-148">На странице списка желаний отображаются номенклатуры, добавленные в список желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="21df7-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="21df7-149">Она использует модуль списка желаний для отображения номенклатур списка желаний.</span><span class="sxs-lookup"><span data-stu-id="21df7-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="21df7-150">Страница лояльности</span><span class="sxs-lookup"><span data-stu-id="21df7-150">Loyalty page</span></span>

<span data-ttu-id="21df7-151">Страница программы лояльности позволяет клиентам присоединиться к программе лояльности или, если они уже являются участниками программы лояльности, просмотреть сведения о программе.</span><span class="sxs-lookup"><span data-stu-id="21df7-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="21df7-152">Они также могут просматривать заработанные и погашенные баллы в последних проводках.</span><span class="sxs-lookup"><span data-stu-id="21df7-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21df7-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="21df7-153">Additional resources</span></span>

[<span data-ttu-id="21df7-154">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="21df7-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="21df7-155">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="21df7-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="21df7-156">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="21df7-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="21df7-157">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="21df7-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="21df7-158">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="21df7-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="21df7-159">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="21df7-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="21df7-160">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="21df7-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="21df7-161">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="21df7-161">Footer module</span></span>](author-footer-module.md)
