---
title: При создании строк заказа на продажу выбрано одно и то же коммерческое соглашение
description: Если для определенной даты задано более одного коммерческого соглашения, при создании строк заказа на продажу всегда выбирается соглашение с наименьшей ценой.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477421"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Если существуют два коммерческих соглашения с пересекающимися датами, всегда выбирается только одно из них

## <a name="symptoms"></a>Симптомы

Если для одного и того же периода или перекрывающихся периодов определены два коммерческих соглашения, то при создании строк заказа на продажу, содержащих эти номенклатуры, всегда выбирается одно и то же коммерческое соглашение.

## <a name="resolution"></a>Решение

Если для определенной даты имеется более одного коммерческого соглашения, всегда выбирается коммерческое соглашение с наименьшей ценой. Для получения дополнительных сведений загрузите следующий технический документ: [Коммерческие соглашения в Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
