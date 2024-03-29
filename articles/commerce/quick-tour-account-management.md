---
title: Обзор страниц управления учетными записями
description: В этой статье представлен обзор страниц управления учетными записями в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 126df38f8c3db6de67e5e0436e48deddd4d8e08b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292117"
---
# <a name="account-management-pages-overview"></a>Обзор страниц управления учетными записями

[!include [banner](includes/banner.md)]

В этой статье представлен обзор страниц управления учетными записями в Microsoft Dynamics 365 Commerce.

Страницы управления учетными записями позволяют клиентам просматривать сведения, имеющие отношение к их учетным записям и заказам. Страницы управления учетными записями включают целевую страницу управления учетными записями и страницы для профиля пользователя, адресов, журнала заказов, сведений о заказе, баллов по программы лояльности и списка желаний.

### <a name="account-management-landing-page"></a>Целевая страница управления учетной записью

Когда клиент выполняет вход и выбирает пункт **Моя учетная запись**, открывается целевая страница управления учетными записями. На этой странице содержится краткая сводка по всем сведениям, относящимися к данной учетной записи, такие как профиль пользователя, заказы, список желаний, адреса, баллы по программе лояльности. С этой страницы у клиента может быть доступ к дополнительным сведениям для каждой области.

На следующем рисунке показан пример целевой страницы управления учетными записями.

![Пример целевой страницы управления учетной записью.](./media/Account-Management.PNG)

### <a name="my-profile-page"></a>Страница "Мой профиль"

На странице **Мой профиль** отображаются сведения об учетной записи клиента, такие как имя и номер телефона. Клиент может обновить сведения о своем профиле на этой странице. Эту страницу можно настроить таким образом, чтобы она включала дополнительные настройки учетной записи клиента, такие как параметр для согласия на получение маркетинговых сообщений электронной почты.

На следующем рисунке показан пример страницы **Мой профиль**, которая была создана с помощью библиотеки модулей.

![Пример страницы "Мой профиль".](./media/Account-Management-MyProfile.PNG)

### <a name="addresses-page"></a>Страница адресов

Страница **Адреса** позволяет клиенту добавлять адреса в свою учетную запись. Здесь также отображается список адресов, которые клиент ранее добавил или сохранил в учетной записи. Эти адреса являются адресами, введенными клиентом либо на данной странице, либо при размещении заказа.

На следующем рисунке показан пример страницы **Адреса**.

![Пример страницы адресов.](./media/Account-Management-Address.png)

### <a name="order-history-and-order-details-pages"></a>Страницы истории заказов и сведений о заказе

На странице **История заказов** отображается сводка по всем заказам, отправленным клиентом с помощью своей учетной записи. Она предоставляет быструю сводку по заказанным номенклатурам, номер подтверждения, код продажи, сведения для отслеживания и другую информацию. Если клиент хочет просмотреть более детализированную разбивку для каждого заказа, имеется страница **Сведения о заказе**. Эта страница включает такие сведения, как адрес доставки, сведения о платежах, скидки, налоги и затраты на доставку по данному заказу.

На следующем рисунке показан пример страницы **История заказов**.

![Пример страницы истории заказов.](./media/Account-Management-OrderHistory.PNG)

На следующем рисунке показан пример страницы **Сведения о заказе**.

![Пример страницы сведений о заказе.](./media/Account-Management-OrderDetails.PNG)

### <a name="loyalty-program-page"></a>Страница программы лояльности

Страница **Программа лояльности** позволяет клиенту стать членом программы лояльности. После регистрации клиента в программе лояльности страница **Программа лояльности** включает такие сведения, как количество заработанных баллов и число баллов, которые были погашены.

Следующая иллюстрация показывает пример страницы **Программа лояльности**.

![Пример страницы программы лояльности.](./media/Account-Management-Loyalty.PNG)

### <a name="wishlist-page"></a>Страница списка пожеланий

Страница **Список желаний** содержит список номенклатур, добавленных клиентом в свой список желаний. В список желаний можно добавить продукты и варианты продуктов. С этой страницы клиент может удалить номенклатуру из списка желаний или добавить номенклатуру непосредственно в корзину.

Следующая иллюстрация показывает пример страницы **Список желаний**.

![Пример страницы списка желаний.](./media/Account-Management-Wishlist.PNG)

Дополнительные сведения о модулях управления учетными записями и способах их создания см. в разделе [Управление учетными записями](account-management.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор домашней страницы](quick-tour-home-page.md)

[Обзор страниц сведений о продукте](quick-tour-pdp.md)

[Обзор страниц корзины и оформления заказа](quick-tour-cart-checkout.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
