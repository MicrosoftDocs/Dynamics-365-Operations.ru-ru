---
title: Обзор сводного планирования и функции работы с несколькими узлами
description: При сводном планировании учитываются настройки складских аналитик сайта и склада.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b26ff5c2f580c30113b82302bbad744bbf285ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213730"
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



