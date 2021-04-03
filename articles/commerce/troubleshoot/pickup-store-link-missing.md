---
title: Параметр "Забрать это" не отображается на страницах "Корзина" или "сведения о продукте"
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что параметр для самовывоза из магазина не появился на странице корзины или на страницах сведений о продукте.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585498"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Параметр "Забрать это" не отображается на страницах "Корзина" или "сведения о продукте"

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь в том, что параметр для самовывоза из магазина не появился на странице корзины или на страницах сведений о продукте.

## <a name="description"></a>описание

Кнопка **Забрать это** не отображается на страницах "Корзина" или "сведения о продукте".

На следующем рисунке показан пример страницы, которая включает кнопку **Забрать это**.

![Кнопка "Забрать это"](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Приказ

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Включение расширения BOPIS в конструкторе сайтов Commerce

Чтобы включить функцию "купить в Интернете, забрать в магазине" (BOPIS) в конструкторе сайтов Commerce, выполните следующие действия.

1. Выберите ваш сайт.
1. Выберите **Параметры сайта**, затем выберите **Расширения**.
1. Убедитесь, что флажок **Отключить BOPIS** снят.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Настройка способов доставки в Commerce headquarters

Чтобы настроить способы доставки в Commerce Headquarters, выполните следующие шаги.

1. Переход к **Закупки и источники \> Настройка \> Способы доставки**.
1. Убедитесь, что был создан режим доставки **Самовывоз клиентом**, и что продукты и адреса назначены ему.
1. Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры**.
1. В левой области переходов выберите **Клиентские заказы**.
1. Убедитесь, что **Способ доставки для самовывоза** настроен правильно.

### <a name="configure-customer-orders-payments"></a>Настройка платежей по заказам клиентов

Чтобы настроить платежи по заказам клиентов в Commerce headquarters, выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры**.
1. В левой области переходов выберите **Клиентские заказы**.
1. На экспресс-вкладке **Платежи** убедитесь, что **условия оплаты** и **Способ оплаты** настроены правильно.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка BOPIS](../cpe-bopis.md)

[Включение нескольких режимов доставки самовывозом для заказов клиентов](../multiple-pickup-modes.md)

[Платежи по заказам Commerce многоканального взаимодействия](../dev-itpro/commerce-payments.md)

[Модуль выбора магазина](../store-selector.md)
