---
title: Невозможно выставить накладную на заказ на продажу, направленный клиенту
description: После включения параметра автоматической разноски накладной больше нельзя выставлять накладную по исходному заказу на продажу и исходной прямой поставке.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026843"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Невозможно выставить накладную на заказ на продажу, направленный клиенту

Номер статьи базы знаний: 4611793

## <a name="symptoms"></a>Симптомы

После включения параметра **Автоматическая разноска накладной** на странице **Внутрихолдинговый** для поставщика больше нельзя выставлять накладную по исходному заказу на продажу и исходной прямой поставке.

## <a name="resolution"></a>Приказ

Поведение синхронизации для внутрихолдинговых накладных по заказу и прямых поставок управляется и переопределяется параметрами, описанными в разделе [Настройка параметров для разноски внутрихолдингового заказа](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

После настройки этих параметров сначала необходимо выставить накладную по внутрихолдинговому заказу на продажу. Затем будут синхронизованы исходные заказы на продажу и заказы на покупку.
