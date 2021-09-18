---
title: В приходе по заказу на покупку не включаются все расходы
description: В приходе по заказу на покупку не включаются все расходы
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477374"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>В приходе по заказу на покупку не включаются все расходы

## <a name="symptoms"></a>Симптомы

При получении заказа на покупку не все расходы включаются в поступлении.

### <a name="reproduce-the-issue"></a>Воспроизведение проблемы

Следующая процедура показывает один из способов воспроизведения проблемы.

1. На странице **Параметры модуля "Закупки и источники"** на вкладке **Доставка** убедитесь, что для параметра **Формировать накладные расходы при приходе продукта** установлено значение *Да*.
1. Создайте заказ на покупку, включающий накладные расходы.
1. Подтвердите заказ на покупку.
1. Получите заказ на покупку.
1. Просмотрите итоговую сумму прихода и сравните ее с ожидаемым итогом.
1. Обратите внимание, что не все накладные расходы включены в приход заказа на покупку.

## <a name="resolution"></a>Решение

Разрешение зависит от способа настройки накладных расходов. Сведения о порядке настройки накладных расходов, чтобы они удовлетворяли вашим требованиям, см. в следующей записи блога: [Разноска накладных расходов в момент поступления продуктов](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
