---
title: Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества
description: Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026858"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества

Номер статьи базы знаний: 4612803

## <a name="symptoms"></a>Симптомы

Поле **Дата последнего испытания** не обновляется при создании нескольких заказов контроля качества.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Дата последнего испытания не связана с заказами контроля качества. В ней хранится дата, когда готовые товары были приобретены или произведены впервые. Эта дата используется для расчета даты уведомления о сроке хранения.
