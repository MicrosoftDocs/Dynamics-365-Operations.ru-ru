---
title: Обзор сводного планирования и функции работы с несколькими узлами
description: При сводном планировании учитываются настройки складских аналитик сайта и склада.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e594cfd71201c6a629c04d5557c117649e6b19b0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982337"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Обзор сводного планирования и функции работы с несколькими узлами

[!include [banner](../includes/banner.md)]

При сводном планировании учитываются настройки складских аналитик сайта и склада. 

Аналитика сайта является обязательной; аналитику склада можно настроить как обязательную.

Если аналитика является обязательной, значение этой аналитики должно быть введено во всех складских проводках. Поэтому при сводном планировании узел и склад для начального спроса известны. Аналитика узла также согласована, так что во время развертывания спроса нижнего уровня значение узла не изменяется.

Если склад не настроен как обязательный, он может быть неизвестен для начального спроса. Механизм планирования должен определить, какой склад использовать, на основе настроек, которые определяются для номенклатуры, отдельных складов и сведений строки заказа.

Следующие разделы описывают работу механизма планирования с различными настройками для определения склада, который необходимо использовать.

[Сводное планирование для покрытия сайта и склада, склад обязателен](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Сводное планирование для покрытия сайта, обязательный склад](master-plan-site-coverage-warehouse-mandatory.md)

[Сводное планирование для покрытия сайта и склада, склад не обязателен](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Сводное планирование для покрытия объекта, склад не обязателен](master-plan-site-coverage-warehouse-not-mandatory.md)

[Определение версии спецификации](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]