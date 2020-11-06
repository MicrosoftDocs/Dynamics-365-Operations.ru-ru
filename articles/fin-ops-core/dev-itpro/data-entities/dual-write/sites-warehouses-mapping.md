---
title: Интегрированные сайты и склады
description: Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997633"
---
# <a name="integrated-sites-and-warehouses"></a>Интегрированные объекты и склады

[!include [banner](../../includes/banner.md)]



Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Common Data Service. Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management. Они используются для моделирования цепочки поставок компании.

## <a name="templates"></a>Шаблоны

При интеграции с Common Data Service эти концепции и все связанные с ними сведения доступны в Common Data Service с использованием информационных объектов сайтов и складов в следующей таблице.

Приложения Finance and Operations | Другие приложения Dynamics 365 | Описание
--------------------------|---------------------------|---
Сайты | msdyn_operationalsites | 
Склады | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

