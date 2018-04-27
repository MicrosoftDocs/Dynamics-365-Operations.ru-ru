---
title: "Сводное планирование и функция работы с несколькими узлами"
description: "При сводном планировании учитываются настройки складских аналитик сайта и склада."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6800668741bfd86555b72faf8cce01f73cb9a278
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-and-multisite-functionality"></a>Сводное планирование и функция работы с несколькими узлами

[!INCLUDE [banner](../includes/banner.md)]

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




