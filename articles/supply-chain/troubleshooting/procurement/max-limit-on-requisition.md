---
title: Максимальное ограничение по договору покупки не эффективно для заявки на закупку
description: Максимальное ограничение по договору покупки не эффективно для заявки на закупку
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477394"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Максимальное ограничение по договору покупки не эффективно для заявки на закупку

## <a name="symptoms"></a>Симптомы

Когда заявка на закупку связана с договором покупки, максимальная граница из договора покупки не действует в отношении данной заявки на закупку. Сведения о цене по умолчанию введены правильно, но в заявке на закупку может быть заказано больше максимально допустимого лимита из договора покупки.

## <a name="resolution"></a>Решение

Это поведение является ожидаемым. Поскольку заявки не всегда утверждены, в договоре покупки не следует резервировать количество или сумму. Следовательно, максимальная граница из договора покупки не будет достигнута.
