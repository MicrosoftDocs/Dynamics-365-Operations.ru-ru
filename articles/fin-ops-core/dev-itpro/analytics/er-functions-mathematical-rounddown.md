---
title: Функция ER ROUNDDOWN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ROUNDDOWN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915863"
---
# <a name="ROUNDDOWN">Функция ER ROUNDDOWN</a>

[!include [banner](../includes/banner.md)]

Функция `ROUNDDOWN` возвращает указанное число в виде *вещественного* значения после его округления вниз до указанного числа десятичных знаков.

## <a name="syntax"></a>Синтаксис

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный*

Числовое значение, которое должно быть округлено вниз.

`decimals`: *Целочисленный*

Числовое значение, представляющее количество десятичных знаков.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция поступает как [ROUND](er-functions-mathematical-round.md), но она всегда округляет указанное число вниз (в направлении нуля).

## <a name="example-1"></a>Пример 1

`ROUNDDOWN (1200.767, 2)` округляет вниз до двух десятичных знаков и возвращает **1200.76**. 

## <a name="example-2"></a>Пример 2

`ROUNDDOWN (1700.767, -3)` округляет вниз до ближайшего числа, кратного тысяче, и возвращает **1000**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)
