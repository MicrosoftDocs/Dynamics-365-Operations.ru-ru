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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 1b9181211bbb65cdfc46e63f3cee0e9f5bc9f6a4
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173070"
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

