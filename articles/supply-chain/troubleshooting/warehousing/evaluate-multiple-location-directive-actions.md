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
ms.openlocfilehash: ea265166902f85c2c09cae08ee6de5cd7094e1b4
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778410"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Параметр с несколькими SKU не оценивает действия директивы по нескольким местоположениям

## <a name="symptoms"></a>Симптомы

Директивы местоположения типа заказа на работу *Заказы на продажу* и типа работы *Размещение* не оценивают несколько действий директивы местоположения при выборе параметра **Несколько SKU**. Оценивается только действие директивы первого местоположения.

## <a name="resolution"></a>Решение

Новая функция *Оценивать все действия для директив местоположения с несколькими SKU* была добавлена в версии 10.0.15 (см. статью базы знаний [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Эта функция оценивает все действия для директив местоположения с несколькими единицами складского учета SKU. В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. Администраторы могут использовать страницу [управления функциями](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения или выключения их при необходимости.
