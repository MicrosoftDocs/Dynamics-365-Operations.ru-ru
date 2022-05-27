---
title: Панель фильтра на странице списка количества в наличии не работает должным образом
description: Фильтры на панель фильтра на странице "Список запасов в наличии" не фильтрует результаты так, как вы ожидаете.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686693"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Панель фильтра на странице списка количества в наличии не работает должным образом

## <a name="symptoms"></a>Симптомы

Фильтры на панель фильтра на странице **Список запасов в наличии** не фильтрует результаты так, как вы ожидаете.

## <a name="resolution"></a>Решение

Страница **Список запасов в наличии** составляется из подробной таблицы запасов в наличии, которая включает все доступные аналитики. Однако список на этой странице является сводным. Таким образом, это может быть сочетание строк из исходной таблицы путем агрегирования значений в соответствии с отображаемыми аналитиками.

Фильтры, которые настроены в области фильтров, применяются к исходной таблице, а не к сводному списку. Такое поведение может иногда привести к неожиданным результатам, как показано в [следующих примерах](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

Однако, [указанные в сетке фильтры](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters) *применяются* к сводному списку. К этим фильтрам относятся QuickFilter в верхней части сетки и фильтр для каждого заголовка столбца.
