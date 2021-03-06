---
title: Код поставщика не авторизован для определенного продукта и даты
description: При попытке утверждения спланированного заказа или добавления строки в заказ на покупку будет выведено сообщение об ошибке, в котором говорится, что код поставщика не авторизован для продукта и даты.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294167"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Код поставщика не авторизован для определенного продукта и даты

Код ошибки: SYP4881415

## <a name="symptoms"></a>Симптомы

При попытке утвердить спланированный заказ или добавить строку в заказ на покупку выводится следующее сообщение об ошибке:

> Код поставщика %1 не разрешен для действия "%2" в %3.

## <a name="cause"></a>Причина

Ошибка возникает из-за того поле **Способ проверки утвержденных поставщиков** имеет значение *Только предупреждение* или *Не разрешено* для указанного продукта, и поставщик не авторизован для поставки этого продукта в данный момент.

## <a name="resolution"></a>Решение

Чтобы решить эту проблему, отключите проверку поставщика для соответствующего продукта или утвердите поставщика.

Чтобы отключить проверку продукта для поставщика, выполните следующие действия.

1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
1. Откройте соответствующий продукт.
1. На экспресс-вкладке **Покупка** задайте в поле **Способ проверки утвержденных поставщиков** значение, отличное от *Только предупреждение* или *Не разрешено*.

Чтобы утвердить поставщика для продукта, выполните следующие действия.

1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
1. Откройте соответствующую номенклатуру.
1. В области действий на вкладке **Покупка** в группе **Утвержденный поставщик** выберите **Настройка**.
1. На странице списка **Утвержденный поставщик** добавьте строку в сетку и установите для нее следующие значения:

    - **Поставщик** — выберите поставщика, которого необходимо утвердить для текущего продукта.
    - **Дата вступления в силу** — выберите первую дату, для которой утвержден поставщик.
    - **Дата окончания срока действия** — выберите последнюю дату, для которой утвержден поставщик.

Для дополнительной информации см. [Утверждение поставщиков для определенных продуктов](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
