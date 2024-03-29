---
title: Гибридные клиентские заказы
description: Гибридный клиентский заказ представляет собой один заказ, содержащий продукты, которые клиент может унести с собой из магазина, а также продукты, которые он заберет или которые будут доставлены позже.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4cb448670af9a6ddce8008be008cf3b0ff76bbce65053bf4618ea6668c4568d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739537"
---
# <a name="hybrid-customer-orders"></a>Гибридные клиентские заказы

[!include [banner](includes/banner.md)]

Гибридный клиентский заказ представляет собой один заказ, содержащий продукты, которые клиент может унести с собой из магазина, а также продукты, которые он заберет или которые будут доставлены позже.

В Commerce для заказа клиента можно выбрать, что клиент заберет все продукты или заберет выбранные продукты. Для строк продуктов, помеченных как "на вынос", автоматически выставляется накладная после создания заказа, аналогично тому, как для заказа, который клиент заберет после создания заказа. Суммы, подлежащая оплате по гибридным заказам, определяется путем добавления процента депозита по строкам комплектации и отгрузки товаров к полной сумме строка "на вынос". Для гибридных заказов система переключается между режимом заказа клиента и режимом "оплатил наличными и забрал" следующим образом:

- Если все товары в корзине заданы как установлены как **Способ поставки "На вынос"**, заказ будет обрабатываться как проводка "Продажа без доставки при оплате наличными".
- Если для какой-либо строки или всех строк в корзине задана **Комплектация** или **Доставка**, заказ будет обрабатываться как проводка заказа клиента.

Если строка корзины выбрана и выбрано значение **Отобрать выбранное**, **Отгрузить выбранные** или **Вынести выбранные**, этот метод доставки будет установлен только для конкретной строки корзины. В этом случае дальнейший поток операций продолжается в обычном режиме. Однако если значение **Отобрать выбранное**, **Отгрузить выбранные** или **Вынести выбранные** выбрано, когда никакая строка корзины не выбрана, открывается новая страница, на которой отображаются все строки корзины. На этом окне можно выбрать несколько строк за один раз, чтобы задать способ доставки. При использовании этого метода для выбора строк будут переопределены все предыдущие методы доставки, назначенные данной строке.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Клиентские заказы в Modern POS (MPOS)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]