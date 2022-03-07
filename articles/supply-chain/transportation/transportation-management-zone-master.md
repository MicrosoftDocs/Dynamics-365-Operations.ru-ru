---
title: Шаблон зоны управления транспортировкой
description: В этой теме объясняется, как управление транспортировкой позволяет разделить географические местоположения на зоны.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "4436505"
---
# <a name="transportation-management-zone-master"></a>Шаблон зоны управления транспортировкой

[!include [banner](../includes/banner.md)]

Управление транспортировкой позволяет разделить географические местоположения на зоны. Деление местоположения на зоны помогает:

- **Упростить ценообразование транспортировки** — ценообразование по зонам может быть более простыми, чем отдельные цены на основе местоположения, особенно когда местоположения транспортировки разбросаны по всему местоположению.
- **Оптимизировать планирование загрузки** — путем консолидации загрузок по зонам.
- **Оптимизировать планирование маршрутов** — назначая отдельные планы маршрутов отдельным зонам.

Зоны определяются на основе значений полей метаданных (например, страна/регион, диапазон почтовых индексов или услуга перевозчика), которые квалифицируют каждую зону. Определения зон не требуются, если в ценах транспортировки не используется концепция зон.
