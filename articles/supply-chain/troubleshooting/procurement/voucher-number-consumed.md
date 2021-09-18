---
title: Код ваучера поступления продукта используется даже без создания ваучера
description: Код операции прихода продукта потребляется даже в том случае, если финансовая операция во время поступления продуктов не создается.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477410"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Код ваучера поступления продукта используется даже без создания ваучера

## <a name="symptoms"></a>Симптомы

Код операции прихода продукта потребляется даже в том случае, если финансовая операция во время поступления продуктов не создается.

## <a name="resolution"></a>Решение

Если для параметра **Начисление задолженности при поступлении продуктов** задано значение *Нет* для группы моделей номенклатуры, разноска в главную книгу производиться не будет. Однако для учета в субкниге регистрируется физическое событие, а для этого события требуется код операции. Этот код операции является кодом операции, на который имеются ссылки в складских проводках.

Рекомендуется установить для параметра **Начисление задолженности при поступлении продуктов** значение *Да*, как описано в следующей записи блога: [Разноска накладных расходов во время получения продукта](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
