---
title: Количество в запущенном карантинном заказе не обновляется при разбиении заказа
description: При создании карантинного заказа и попытке его разбиения количество заказа не обновляется на оставшееся количество после разбивки.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026860"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Количество в запущенном карантинном заказе не обновляется при разбиении заказа

Номер статьи базы знаний: 4613113

## <a name="symptoms"></a>Симптомы

При создании карантинного заказа и попытке его разбиения количество заказа не обновляется на оставшееся количество после разбивки.

## <a name="resolution"></a>Приказ

Система не изменяет исходное количество из карантинного заказа для того, чтобы можно было отслеживать исходное количество, которое было создано для этого карантинного заказа. Однако система отслеживает количество, разбитое из карантинного заказа. Для выполнения этого отслеживания используется поле базы данных с именем `QuantityThatHasSplitIntoOtherQuarantineOrders`. Однако это поле не отображается в пользовательском интерфейсе.
