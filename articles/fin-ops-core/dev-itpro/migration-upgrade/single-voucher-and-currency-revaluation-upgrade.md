---
title: Обновление журналов с одним ваучером и переоценок в валюте
description: В этой теме описывается, как обновить журналы с одним ваучером и переоценки в валюте.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127311"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Обновление журналов с одним ваучером и переоценок в валюте

[!include [banner](../includes/banner.md)]

Некоторые организации вводят журналы, содержащие один ваучер, который имеет несколько клиентов или поставщиков, при этом они также выполняют процесс переоценки расчетов с клиентами или расчетов с поставщиками в иностранной валюте. В этом разделе описаны шаги, которые такие организации должны выполнить при обновлении до Microsoft Dynamics 365 for Operations версии 1611.

Выполните эти шаги при обновлении до Microsoft Dynamics 365 for Operations версии 1611.

1.  Перед обновлением до Finance and Operations выполните процессы переоценки в иностранной валюте для расчетов с клиентами и расчетов с поставщиками. В поле **Метод** установите значение **Дата накладной**. Создается проводка переоценки, которая реверсирует последнюю переоценки в иностранной валюте. Таким образом открытые проводки оцениваются в их исходной валюте учета.
2.  Выполните обновление до версии 1611.
3.  Снова выполните процессы переоценки в иностранной валюте для расчетов с поставщиками и расчетов с клиентами. На этот раз задайте в поле **Метод** значение **Стандартный**. Создается новая проводка переоценки на основании текущих валютных курсов. Эта проводка записывает нереализованные прибыли и убытки на правильный итоговый счет ГК.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]