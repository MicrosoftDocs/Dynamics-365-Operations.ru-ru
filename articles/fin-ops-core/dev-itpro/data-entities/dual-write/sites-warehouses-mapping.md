---
title: Интегрированные сайты и склады
description: Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750674"
---
# <a name="integrated-sites-and-warehouses"></a>Интегрированные объекты и склады

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Эта тема описывает интеграцию сайта и данных склада между Finance and Operations и Dataverse. Операционные сайты и склады являются общими концепциями в приложении Supply Chain Management. Они используются для моделирования цепочки поставок компании.

## <a name="templates"></a>Шаблоны

При интеграции с Dataverse эти концепции и все связанные с ними сведения доступны в Dataverse с использованием информационных таблиц сайтов и складов в следующей таблице.

Приложения Finance and Operations | Другие приложения Dynamics 365 | описание
--------------------------|---------------------------|---
Сайты | msdyn_operationalsites | 
Склады | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]