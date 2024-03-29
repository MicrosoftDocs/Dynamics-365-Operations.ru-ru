---
title: Продажа и возврат продуктов, которые не являются частью ассортимента магазина
description: С Dynamics 365 Commerce можно продавать и возвращать продукты за пределами ассортиментов.
author: josaw1
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.custom: ''
ms.search.industry: retail
ms.search.form: RetailAssortmentDetails
ms.openlocfilehash: d2444d7812cffc832986589825b332d60a508b18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275041"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Продажа и возврат продуктов, которые не являются частью ассортимента магазина

[!include [banner](includes/banner.md)]

Для любого предприятия розничной торговли достаточно распространенным является сценарий с продажей продуктов и приемом возвратов продуктов, даже если эти продукты отсутствуют в магазине (иными словами, продуктов, не входящих в ассортимент магазина).

Вот некоторые типовые сценарии:

+ В конкретном магазине предприятия розничной торговли не выставлены все продукты, которыми торгует предприятие. Остальные продукты хранятся на складе. Сотрудник магазина может помочь клиенту, найдя продукты на складе, добавив их в корзину и оформив заказ путем выбора метода доставки, — например, продукт может быть доставлен со склада по определенному адресу или клиент может забрать его из данного магазина или из другого магазина.
+ В магазине, которые посетил клиент, определенные продукты не выставлены или их нет в наличии, однако эти продукты имеются в других магазинах. Сотрудник магазина помочь клиенту, найдя продукты в другом магазине, добавив их в корзину и оформив заказ путем выбора метода доставки.
+ У предприятия розничной торговли несколько магазинов в конкретном городе или районе, и предприятие не требует, чтобы клиенты возвращали купленные продукты именно в тот магазин, где они их приобрели. Клиенты могут сделать возврат в любом удобном им магазине.

С помощью Commerce предприятия розничной торговли могут реализовать эти типовые сценарии. Система Commerce позволяет:

+ Искать или просматривать продукты в других магазинах.
+ Искать или просматривать все выпущенные в продажу продукты.
+ Создавать проводки "заплатил и забрал" или заказы клиентов.
+ Выбирать варианты доставки для заказов клиентов.
+ Оформлять самовывоз продуктов клиентами из текущего магазина или из другого магазина.
+ Отменять заказы в текущем магазине или в другом магазине.
+ Оформлять возврат заказов с учетом или без учета прихода в текущем магазине или в другом магазине.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
