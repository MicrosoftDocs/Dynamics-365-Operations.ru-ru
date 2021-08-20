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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742036"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Поле "Дата последнего испытания" не обновляется при создании нескольких заказов контроля качества

Номер статьи базы знаний: 4612803

## <a name="symptoms"></a>Симптомы

Поле **Дата последнего испытания** не обновляется при создании нескольких заказов контроля качества.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Дата последнего испытания не связана с заказами контроля качества. В ней хранится дата, когда готовые товары были приобретены или произведены впервые. Эта дата используется для расчета даты уведомления о сроке хранения.
