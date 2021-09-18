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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477445"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Панель фильтра на странице списка количества в наличии не работает должным образом

## <a name="symptoms"></a>Симптомы

Фильтры на панель фильтра на странице **Список запасов в наличии** не фильтрует результаты так, как вы ожидаете.

## <a name="resolution"></a>Решение

Страница  **Список запасов в наличии** составляется из подробной таблицы запасов в наличии, которая включает все доступные аналитики. Однако список на этой странице является сводным. Таким образом, это может быть сочетание строк из исходной таблицы путем агрегирования значений в соответствии с отображаемыми аналитиками.

Фильтры, которые настроены в области фильтров, применяются к исходной таблице, а не к сводному списку. Такое поведение может иногда привести к неожиданным результатам, как показано в [следующих примерах](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Однако,  [указанные в сетке фильтры](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *применяются*  к сводному списку. К этим фильтрам относятся QuickFilter в верхней части сетки и фильтр для каждого заголовка столбца.
