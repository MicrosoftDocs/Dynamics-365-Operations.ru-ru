---
title: Цены за единицу в заказах на покупку не рассчитываются на основе преобразования единиц измерения
description: Цены за единицу в заказах на покупку не рассчитываются на основе преобразования единиц измерения
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
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477411"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Цены за единицу в заказах на покупку не рассчитываются на основе преобразования единиц измерения

## <a name="symptoms"></a>Симптомы

При изменении единицы в заказе на покупку цены коммерческих соглашений не пересчитываются в соответствии с определениями пересчета единиц измерения.

## <a name="cause"></a>Причина

Цены всегда извлекаются из коммерческих соглашениях (или других настроек цен в системе, таких как соглашения о продаже или цены номенклатур), и они настраиваются для единицы измерения.

Если единица измерения изменяется в строке заказа, система выполняет поиск цены для новой единицы измерения и применяет эту цену. Если для единицы измерения цена не найдена, система не применяет цену. Пересчет единиц измерения не может использоваться для пересчета цены в другую единицу измерения. Теоретически цена за один ящик с десятком может не быть равна десяти ценам одного ящика.

## <a name="workaround"></a>Обходное решение

Одним из способов обхода этой проблемы является обеспечение наличия коммерческих соглашений для единиц измерения, которые, как вы ожидаете, будут использоваться в строках заказа для данной номенклатуры.