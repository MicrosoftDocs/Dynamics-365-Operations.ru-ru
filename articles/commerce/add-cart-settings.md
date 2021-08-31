---
title: Применение параметров добавления продукта в корзину
description: В этой теме описываются параметры добавления продукта в корзину, а также описывается, как их применять в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6299a1c815978ab9f748b6110980e673e1fbae927ed08a5e2e080f89ef063115
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712822"
---
# <a name="apply-add-product-to-cart-settings"></a>Применение параметров добавления продукта в корзину

[!include [banner](includes/banner.md)]

В этой теме описываются параметры **добавления продукта в корзину**, а также описывается, как их применять в Microsoft Dynamics 365 Commerce.

При добавлении продукта в корзину на сайте электронной коммерции Dynamics 365 Commerce поддерживаются разные бизнес-правила. Например, пользователь сайта может быть перенаправлен на страницу корзины. Или же, пользователь может остаться на текущей странице, но получить уведомление о том, что продукт был добавлен в корзину.

Для поддержки других бизнес -процессов поле **Добавить продукт в корзину** доступно в **Параметры \> Расширения** в конфигураторе сайта Commerce. Выберите один из следующих параметров настройки для реализации соответствующего бизнес-процесса:

- **Перейти к странице корзины** — когда пользователи добавляют номенклатуру в корзину, они направляются на страницу корзины.
- **Показать уведомление** — когда пользователи добавляют номенклатуру в корзину, они получают уведомление о подтверждении и могут продолжать просматривать страницу сведений о продукте (PDP).
- **Показать мини-корзину** — когда пользователи добавляют номенклатуру в корзину, отображается содержимое мини-корзины. Пользователи могут просматривать все номенклатуры в корзине, и при готовности могут перейти к оформлению заказа.
- **Показать уведомление с помощью модуля уведомлений** — когда пользователи добавляют номенклатуру в корзину, модуль уведомлений используется для отображения уведомления о подтверждении. Чтобы этот параметр работал, модуль уведомлений должен быть добавлен в заголовок страницы.
- **Не переходить на страницу корзины** — когда пользователи добавляют номенклатуру в корзину, они остаются на текущей странице.

На следующем рисунке показан пример параметров **добавления продукта в корзину** в конфигураторе сайтов.

![Пример параметров добавления продукта в корзину в конфигураторе сайтов](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Параметры сайта **Добавить продукт в корзину** доступны в выпуске Dynamics 365 Commerce 10.0.11. Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json. Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Параметр **Показать мини-корзину** доступен в версии Dynamics 365 Commerce 10.0.20. Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json. Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

На следующем рисунке показан пример уведомления о подтверждении "Добавлено в корзину" на сайте Fabrikam.

![Пример уведомления "Добавлено в корзину" на сайте Fabrikam](./media/ecommerce-addtocart-notifications.PNG)

На следующем рисунке показан пример уведомления о подтверждении "Добавлено в корзину" на сайте Adventure Works.

![Пример уведомления "Добавлено в корзину" на сайте Adventure Works](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор библиотеки модулей](starter-kit-overview.md)

[Модуль поля покупки](add-buy-box.md)

[Модуль выбора магазина](store-selector.md)