---
title: Невозможно удалить выпущенный продукт
description: Удалить выпущенный продукт и все его варианты можно только в том случае, если выпущенный продукт не имеет каких-либо связанных проводок.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477448"
---
# <a name="you-cant-delete-a-released-product"></a>Невозможно удалить выпущенный продукт

## <a name="symptoms"></a>Симптомы

Удалить выпущенный продукт и все его варианты можно только в том случае, если выпущенный продукт не имеет каких-либо связанных проводок.

## <a name="resolution"></a>Решение

Выполните следующие действия, чтобы удалить выпущенный продукт или шаблон продукта.

1. Закройте все открытые проводки по номенклатурам.
1. Сократите запасы до 0 (нуля).
1. Выполните закрытие запасов.
1. Удалите все варианты продуктов для шаблона продукта, который необходимо удалить.
