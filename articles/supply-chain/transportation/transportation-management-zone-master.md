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
# <a name="transportation-management-zone-master"></a><span data-ttu-id="df182-103">Шаблон зоны управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="df182-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df182-104">Управление транспортировкой позволяет разделить географические местоположения на зоны.</span><span class="sxs-lookup"><span data-stu-id="df182-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="df182-105">Деление местоположения на зоны помогает:</span><span class="sxs-lookup"><span data-stu-id="df182-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="df182-106">**Упростить ценообразование транспортировки** — ценообразование по зонам может быть более простыми, чем отдельные цены на основе местоположения, особенно когда местоположения транспортировки разбросаны по всему местоположению.</span><span class="sxs-lookup"><span data-stu-id="df182-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="df182-107">**Оптимизировать планирование загрузки** — путем консолидации загрузок по зонам.</span><span class="sxs-lookup"><span data-stu-id="df182-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="df182-108">**Оптимизировать планирование маршрутов** — назначая отдельные планы маршрутов отдельным зонам.</span><span class="sxs-lookup"><span data-stu-id="df182-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="df182-109">Зоны определяются на основе значений полей метаданных (например, страна/регион, диапазон почтовых индексов или услуга перевозчика), которые квалифицируют каждую зону.</span><span class="sxs-lookup"><span data-stu-id="df182-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="df182-110">Определения зон не требуются, если в ценах транспортировки не используется концепция зон.</span><span class="sxs-lookup"><span data-stu-id="df182-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
