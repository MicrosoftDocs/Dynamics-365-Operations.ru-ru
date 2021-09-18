---
title: Оценка всех действий для директив мест хранения с несколькими SKU
description: Добавлена новая функция для оценки всех действий для директив местоположения с несколькими SKU. На этой странице рассказывается, как ее включить.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477399"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Параметр с несколькими SKU не оценивает действия директивы по нескольким местоположениям

## <a name="symptoms"></a>Симптомы

Директивы местоположения типа заказа на работу *Заказы на продажу* и типа работы *Размещение* не оценивают несколько действий директивы местоположения при выборе параметра **Несколько SKU**. Оценивается только действие директивы первого местоположения.

## <a name="resolution"></a>Решение

Новая функция *Оценивать все действия для директив местоположения с несколькими SKU* была добавлена в версии 10.0.15 (см. статью базы знаний [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Эта функция оценивает все действия для директив местоположения с несколькими единицами складского учета SKU. Если вам требуется эта функция, используйте [Управление функциями](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview), чтобы включить ее.
