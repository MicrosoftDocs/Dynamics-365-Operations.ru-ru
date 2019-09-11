---
title: Обзор сводного планирования и функции работы с несколькими узлами
description: При сводном планировании учитываются настройки складских аналитик сайта и склада.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865420"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Обзор сводного планирования и функции работы с несколькими узлами

[!include [banner](../includes/banner.md)]

При сводном планировании учитываются настройки складских аналитик сайта и склада. 

Аналитика сайта является обязательной; аналитику склада можно настроить как обязательную.

Если аналитика является обязательной, значение этой аналитики должно быть введено во всех складских проводках. Поэтому при сводном планировании узел и склад для начального спроса известны. Аналитика узла также согласована, так что во время развертывания спроса нижнего уровня значение узла не изменяется.

Если склад не настроен как обязательный, он может быть неизвестен для начального спроса. Механизм планирования должен определить, какой склад использовать, на основе настроек, которые определяются для номенклатуры, отдельных складов и сведений строки заказа.

Следующие разделы описывают работу механизма планирования с различными настройками для определения склада, который необходимо использовать.

[Сводное планирование — покрытие объекта и склада, склад является обязательным](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Сводное планирование — покрытие объекта, склад является обязательным](master-plan-site-coverage-warehouse-mandatory.md)

[Сводное планирование — покрытие объекта и склада, склад не является обязательным](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Сводное планирование — покрытие объекта, склад не является обязательным](master-plan-site-coverage-warehouse-not-mandatory.md)

[Сводное планирование — Определение версии спецификации](master-plan-bom-version-determined.md)



