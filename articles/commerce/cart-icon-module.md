---
title: Модуль значка корзины
description: В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411097"
---
# <a name="cart-icon-module"></a>Модуль значка корзины

[!include [banner](includes/banner.md)]

В этом разделе описывается модуль значка корзины, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Модуль значка корзины представляет корзину в модуле заголовка страницы и отображает количество номенклатур в корзине. В модуле значка корзины также отображается сводка по корзине (также называется мини-корзиной), когда на значок корзины наводится указатель. Мини-корзина предоставляет пользователю сводку номенклатур в корзине без перехода на страницу корзины. Кроме того, она позволяет пользователю непосредственно перейти на страницу оформления заказа, если его устраивает сводка. Это позволяет сократить число переходов между страницами и ускорить оформление. 

На следующем рисунке показан пример модуля значка корзины, в котором отображается мини-корзина в заголовке Fabrikam.

![Пример модуля значка корзины](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Свойства модуля

- **Показать мини- корзину** — если задано значение true, это свойство позволяет отображать сводку корзины (мини-корзину), когда указатель наводится на значок корзины. Эта функциональная возможность поддерживается только для портов просмотра рабочего стола.


## <a name="add-a-cart-icon-module-to-a-page"></a>Добавление модуля значка корзины на страницу

Чтобы добавить модуль значка корзины, см. раздел [Модуль заголовка](author-header-module.md).


## <a name="additional-resources"></a>Дополнительные ресурсы

[Модуль поля покупки](add-buy-box.md)

[Модуль корзины](add-cart-module.md)

[Модуль оформления заказа](add-checkout-module.md)

[Модуль подтверждения заказа](order-confirmation-module.md)

[Модуль заголовка](author-header-module.md)

[Модуль нижнего колонтитула](author-footer-module.md)
