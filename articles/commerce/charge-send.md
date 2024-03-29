---
title: Отгрузка заказов из другого магазина с помощью функции отправки накладных расходов
description: В этой статье описывается функция отправки накладных расходов.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: d73a21bfe9a284bd6e222e73bb0250648912b230
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863521"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Отгрузка заказов из другого магазина с помощью функции отправки накладных расходов

[!include [banner](includes/banner.md)]

С помощью функции отправки накладных расходов в Commerce заказы клиента могут быть размещены в одном магазине и отгружены из другого магазина.

Заказы клиента в клиенте POS-терминала поддерживают несколько вариантов исполнения. Некоторые примеры вариантов выполнения приведены ниже.

- Получение в том же магазине в другой день.
- Получение в другом магазине в этот же или в другой день.
- Отгрузка со склада отгрузки по умолчанию, который назначен магазину, и доставка в определенную дату.

Функция отправки накладных расходов использует следующие операции POS-терминала: "Отгрузить все продукты" и "Отгрузить выбранные продукты". Это позволяет служащему магазина выбрать "место отгрузки", из которого может быть выполнен заказ или строка заказа. По умолчанию "место отгрузки" — это склад отгрузки, который связан с магазином. Однако служащий магазина может изменить этот склад и выбрать любой магазин, который определен в группе локатора магазина, которая назначена магазину.

Возможность выбора адреса "доставки" остается неизменной.

Методы доставки, которые можно использовать для выполнения строки заказа, основаны на конфигурации допустимых способов доставки продуктов и адресов. Поскольку правила в отношении допустимых способов доставки поддерживаются только в центральном офисе (HQ), клиент POS-терминала выполняет вызов в режиме реального времени для выборки допустимых способов доставки для строки отгрузки.


[!INCLUDE[footer-include](../includes/footer-banner.md)]