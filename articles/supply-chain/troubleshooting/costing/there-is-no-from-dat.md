---
title: На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата"
description: На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата".
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026862"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>На вкладке "Активные цены" на странице "Цена номенклатуры" нет значения "Начальная дата"

Номер статьи базы знаний: 4613548

## <a name="symptoms"></a>Симптомы

На вкладке **Активные цены** на странице **Цена номенклатуры** нет значения **Начальная дата**.

## <a name="resolution"></a>Приказ

Значение **Начальная дата** (дата вступления в силу), установленное для ожидающей цены, не переносится в активную цену.

Когда запись стоимости номенклатуры вводится первоначально, она имеет статус *Ожидание* и заданную дату начала действия. При активации записи стоимости номенклатуры происходит обновление статуса на *Активный* и даты начала действия на дату активации. Таким образом, дата активации активной цены всегда является фактической датой активации.

Дополнительные сведения см. в разделе [Обзор версий учета затрат](../../cost-management/costing-versions.md).
