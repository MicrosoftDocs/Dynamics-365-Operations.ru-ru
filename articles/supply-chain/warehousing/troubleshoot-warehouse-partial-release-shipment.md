---
title: Устранение неполадок частичных отпусков и частичных отгрузок
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с частичными отпусками и частичными отгрузками в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645956"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Устранение неполадок частичных отпусков и частичных отгрузок

[!include [banner](../includes/banner.md)]

В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с частичными отпусками и частичными отгрузками в Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Статус выпуска заказа на продажу остается частично отпущенным даже после того, как выставляется накладная по заказу на продажу.

### <a name="issue-description"></a>Описание проблемы

Заказ на продажу является заказом на поставку, но одна или несколько номенклатур в нем имеют другой способ поставки. После выставления накладной по заказу он по-прежнему имеет статус отпуска *Частично отпущен*.

Например, заказ на продажу содержит две номенклатуры: одну для доставки, а другую для получения самовывозом. Были выполнены как доставка, так и получение самовывозом. Поэтому по обеим строкам были выставлены накладные. Однако статус отпуска по-прежнему отображается как *Частично отпущенный*, что является ошибочным.

### <a name="issue-resolution"></a>Устранение проблемы

Статус отпуска применяется только к строкам заказа, для которых номенклатуры включены для управления складом. Таким образом, статус отпуска остается *Частично отпущен* в этом сценарии. Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции. Расширение может быть добавлено как часть отборочной накладной и процесса выставления накладных, чтобы обновить статус отпуска.
